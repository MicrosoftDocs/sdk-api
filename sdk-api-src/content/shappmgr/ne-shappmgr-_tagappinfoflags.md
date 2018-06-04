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

# _tagAppInfoFlags enumeration


## -description


Specifies application information to return from <a href="https://msdn.microsoft.com/8842c12e-2b59-49d6-8140-5a402509a0dd">IShellApp::GetAppInfo</a>. These flags are bitmasks used in the <a href="https://msdn.microsoft.com/3560b088-d899-4fb2-a47c-101f8f5e3bf7">dwMask</a> member of the <b>APPINFODATA</b> structure.


## -enum-fields




### -field AIM_DISPLAYNAME

Returns the display name.


### -field AIM_VERSION

Returns the version.


### -field AIM_PUBLISHER

Returns the application publisher.


### -field AIM_PRODUCTID

Returns the application's product ID.


### -field AIM_REGISTEREDOWNER

Returns the application's registered owner.


### -field AIM_REGISTEREDCOMPANY

Returns the application's registered company.


### -field AIM_LANGUAGE

Returns the language.


### -field AIM_SUPPORTURL

Returns the support URL.


### -field AIM_SUPPORTTELEPHONE

Returns the support telephone number.


### -field AIM_HELPLINK

Returns the Help link.


### -field AIM_INSTALLLOCATION

Returns the application's install location.


### -field AIM_INSTALLSOURCE

Returns the install source.


### -field AIM_INSTALLDATE

Returns the application's install date.


### -field AIM_CONTACT

Returns the application's contact information.


### -field AIM_COMMENTS

Returns application comments.


### -field AIM_IMAGE

Returns the application image.


### -field AIM_READMEURL

Returns the URL of the application's ReadMe file.


### -field AIM_UPDATEINFOURL

Returns the URL of the application's update information.


#### - AIM_REQUIREDBYPOLICY

Obsolete.


## -remarks



Add/Remove Programs in Control Panel uses only <b>AIM_DISPLAYNAME</b> and <b>AIM_SUPPORTURL.</b>



