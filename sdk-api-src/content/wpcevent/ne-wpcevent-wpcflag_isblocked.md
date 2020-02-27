---
UID: NE:wpcevent.tagWPCFLAG_ISBLOCKED
title: WPCFLAG_ISBLOCKED (wpcevent.h)
description: Indicates information about what events are blocked from use and what controls are in place.
old-location: parcon\wpcflag_isblocked.htm
tech.root: parcon
ms.assetid: d8ddea59-04be-4d03-a792-866d8f920e17
ms.date: 12/05/2018
ms.keywords: WPCFLAG_ISBLOCKED, WPCFLAG_ISBLOCKED enumeration, WPCFLAG_ISBLOCKED_ATTACHMENTBLOCKED, WPCFLAG_ISBLOCKED_BADPASS, WPCFLAG_ISBLOCKED_CATEGORYBLOCKED, WPCFLAG_ISBLOCKED_CATEGORYNOTINLIST, WPCFLAG_ISBLOCKED_CONTACTBLOCKED, WPCFLAG_ISBLOCKED_DESCRIPTORBLOCKED, WPCFLAG_ISBLOCKED_DOWNLOADBLOCKED, WPCFLAG_ISBLOCKED_EMAILBLOCKED, WPCFLAG_ISBLOCKED_EXPLICITBLOCK, WPCFLAG_ISBLOCKED_FEATUREBLOCKED, WPCFLAG_ISBLOCKED_GAMESBLOCKED, WPCFLAG_ISBLOCKED_IMBLOCKED, WPCFLAG_ISBLOCKED_INTERNALERROR, WPCFLAG_ISBLOCKED_MAXHOURS, WPCFLAG_ISBLOCKED_MEDIAPLAYBACKBLOCKED, WPCFLAG_ISBLOCKED_NOACCESS, WPCFLAG_ISBLOCKED_NOTBLOCKED, WPCFLAG_ISBLOCKED_NOTEXPLICITLYALLOWED, WPCFLAG_ISBLOCKED_NOTINLIST, WPCFLAG_ISBLOCKED_NOTKIDS, WPCFLAG_ISBLOCKED_RATINGBLOCKED, WPCFLAG_ISBLOCKED_RECEIVERBLOCKED, WPCFLAG_ISBLOCKED_SENDERBLOCKED, WPCFLAG_ISBLOCKED_SETTINGSCHANGEBLOCKED, WPCFLAG_ISBLOCKED_SPECHOURS, WPCFLAG_ISBLOCKED_UNRATED, WPCFLAG_ISBLOCKED_WEBBLOCKED, parcon.wpcflag_isblocked, wpcevent/WPCFLAG_ISBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_ATTACHMENTBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_BADPASS, wpcevent/WPCFLAG_ISBLOCKED_CATEGORYBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_CATEGORYNOTINLIST, wpcevent/WPCFLAG_ISBLOCKED_CONTACTBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_DESCRIPTORBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_DOWNLOADBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_EMAILBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_EXPLICITBLOCK, wpcevent/WPCFLAG_ISBLOCKED_FEATUREBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_GAMESBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_IMBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_INTERNALERROR, wpcevent/WPCFLAG_ISBLOCKED_MAXHOURS, wpcevent/WPCFLAG_ISBLOCKED_MEDIAPLAYBACKBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_NOACCESS, wpcevent/WPCFLAG_ISBLOCKED_NOTBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_NOTEXPLICITLYALLOWED, wpcevent/WPCFLAG_ISBLOCKED_NOTINLIST, wpcevent/WPCFLAG_ISBLOCKED_NOTKIDS, wpcevent/WPCFLAG_ISBLOCKED_RATINGBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_RECEIVERBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_SENDERBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_SETTINGSCHANGEBLOCKED, wpcevent/WPCFLAG_ISBLOCKED_SPECHOURS, wpcevent/WPCFLAG_ISBLOCKED_UNRATED, wpcevent/WPCFLAG_ISBLOCKED_WEBBLOCKED
f1_keywords:
- wpcevent/WPCFLAG_ISBLOCKED
dev_langs:
- c++
req.header: wpcevent.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wpcevent.h
api_name:
- WPCFLAG_ISBLOCKED
targetos: Windows
req.typenames: WPCFLAG_ISBLOCKED
req.redist: 
ms.custom: 19H1
---

# WPCFLAG_ISBLOCKED enumeration


## -description


Indicates information about what events are blocked from use and what controls are in place.


## -enum-fields




### -field WPCFLAG_ISBLOCKED_NOTBLOCKED

No events are blocked from the user.


### -field WPCFLAG_ISBLOCKED_IMBLOCKED

Instant messaging is blocked from the user.


### -field WPCFLAG_ISBLOCKED_EMAILBLOCKED

Email access is blocked from the user.


### -field WPCFLAG_ISBLOCKED_MEDIAPLAYBACKBLOCKED

Playing of media files is blocked from the user.


### -field WPCFLAG_ISBLOCKED_WEBBLOCKED

Internet access is blocked from the user.


### -field WPCFLAG_ISBLOCKED_GAMESBLOCKED

Games are blocked from the user.


### -field WPCFLAG_ISBLOCKED_CONTACTBLOCKED

The contacts list is blocked from the user.


### -field WPCFLAG_ISBLOCKED_FEATUREBLOCKED

Features are blocked from the user.


### -field WPCFLAG_ISBLOCKED_DOWNLOADBLOCKED

The ability to download files is blocked from the user.


### -field WPCFLAG_ISBLOCKED_RATINGBLOCKED

Content with a specified rating is blocked from the user.


### -field WPCFLAG_ISBLOCKED_DESCRIPTORBLOCKED

The description of the content is blocked from the user.


### -field WPCFLAG_ISBLOCKED_EXPLICITBLOCK

Explicit content is blocked from the user.


### -field WPCFLAG_ISBLOCKED_BADPASS

The user has entered a password that is not valid.


### -field WPCFLAG_ISBLOCKED_MAXHOURS

The user has reached the maximum number of hours allowed for computer access.


### -field WPCFLAG_ISBLOCKED_SPECHOURS

The user is blocked from computer access because the time is outside of the specified hours allowed for this user.


### -field WPCFLAG_ISBLOCKED_SETTINGSCHANGEBLOCKED

The user is blocked from changing any computer settings.


### -field WPCFLAG_ISBLOCKED_ATTACHMENTBLOCKED

An attachment is blocked from the user.


### -field WPCFLAG_ISBLOCKED_SENDERBLOCKED

The user is blocked from sending any information to the specified account.


### -field WPCFLAG_ISBLOCKED_RECEIVERBLOCKED

The user is blocked from receiving any information from the specified account.


### -field WPCFLAG_ISBLOCKED_NOTEXPLICITLYALLOWED

The user is blocked because the feature is not explicitly allowed.


### -field WPCFLAG_ISBLOCKED_NOTINLIST

The user is blocked because the feature is not listed as accessible.


### -field WPCFLAG_ISBLOCKED_CATEGORYBLOCKED

The user is blocked from accessing the entire category of activity.


### -field WPCFLAG_ISBLOCKED_CATEGORYNOTINLIST

The user is blocked because the category is not listed as accessible.


### -field WPCFLAG_ISBLOCKED_NOTKIDS

The user is blocked because the rating specifies that the content is not suitable for children.


### -field WPCFLAG_ISBLOCKED_UNRATED

The user is blocked because the content is not rated.


### -field WPCFLAG_ISBLOCKED_NOACCESS

The user is blocked from any access.


### -field WPCFLAG_ISBLOCKED_INTERNALERROR

The user is blocked by an internal error.

