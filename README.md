pyDiscuzRobot
=============

A Robot which realize Discuz API (unofficial).

## Usage

    from DiscuzRobot import DiscuzRobot as DR
    
    # Initial
    r = DR('http://demo.discuz.com/', 'username', 'password')

    # Login
    r.login()

    # Publish, first arg is 'fid'
    r.publish(2, u'Subject', u'Message')

    # Reply, first arg is 'tid'
    r.reply(1, u'Subject', u'Message')

    # Get all fids and their name
    tid_dict = r.get_fid()
    # return [{'fid': '1', 'name': 'forum name'}...]

    # Get all tids and their name
    tid_dict = r.get_tid(3)  # 3 as fid
    # return [{'tid': '1', 'name': 'subject'}...]

    # Get the message
    message = r.get_message(30)  # 30 as tid
