---
UID: NE:shappmgr._tagAppInfoFlags
title: "_tagAppInfoFlags"
author: windows-sdk-content
description: Specifies application information to return from IShellApp::GetAppInfo. These flags are bitmasks used in the dwMask member of the APPINFODATA structure.
old-location: shell\APPINFODATAFLAGS.htm
tech.root: shell
ms.assetid: 80cbc46f-9918-4cca-b41b-1b6caa9c26df
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AIM_COMMENTS, AIM_CONTACT, AIM_DISPLAYNAME, AIM_HELPLINK, AIM_IMAGE, AIM_INSTALLDATE, AIM_INSTALLLOCATION, AIM_INSTALLSOURCE, AIM_LANGUAGE, AIM_PRODUCTID, AIM_PUBLISHER, AIM_READMEURL, AIM_REGISTEREDCOMPANY, AIM_REGISTEREDOWNER, AIM_REQUIREDBYPOLICY, AIM_SUPPORTTELEPHONE, AIM_SUPPORTURL, AIM_UPDATEINFOURL, AIM_VERSION, APPINFODATAFLAGS, APPINFODATAFLAGS enumeration [Windows Shell], _tagAppInfoFlags, inet_APPINFODATAFLAGS, shappmgr/AIM_COMMENTS, shappmgr/AIM_CONTACT, shappmgr/AIM_DISPLAYNAME, shappmgr/AIM_HELPLINK, shappmgr/AIM_IMAGE, shappmgr/AIM_INSTALLDATE, shappmgr/AIM_INSTALLLOCATION, shappmgr/AIM_INSTALLSOURCE, shappmgr/AIM_LANGUAGE, shappmgr/AIM_PRODUCTID, shappmgr/AIM_PUBLISHER, shappmgr/AIM_READMEURL, shappmgr/AIM_REGISTEREDCOMPANY, shappmgr/AIM_REGISTEREDOWNER, shappmgr/AIM_REQUIREDBYPOLICY, shappmgr/AIM_SUPPORTTELEPHONE, shappmgr/AIM_SUPPORTURL, shappmgr/AIM_UPDATEINFOURL, shappmgr/AIM_VERSION, shappmgr/APPINFODATAFLAGS, shell.APPINFODATAFLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - Shappmgr.h
api_name:
 - APPINFODATAFLAGS
product: Windows
targetos: Windows
req.typenames: APPINFODATAFLAGS
req.redist: 
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



