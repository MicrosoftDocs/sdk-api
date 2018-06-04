---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagWPCFLAG_ISBLOCKED enumeration


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

