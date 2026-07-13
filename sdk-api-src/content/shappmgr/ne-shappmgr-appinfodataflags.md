---
UID: NE:shappmgr._tagAppInfoFlags
title: APPINFODATAFLAGS (shappmgr.h)
description: Specifies application information to return from IShellApp::GetAppInfo. These flags are bitmasks used in the dwMask member of the APPINFODATA structure.
helpviewer_keywords: ["AIM_COMMENTS","AIM_CONTACT","AIM_DISPLAYNAME","AIM_HELPLINK","AIM_IMAGE","AIM_INSTALLDATE","AIM_INSTALLLOCATION","AIM_INSTALLSOURCE","AIM_LANGUAGE","AIM_PRODUCTID","AIM_PUBLISHER","AIM_READMEURL","AIM_REGISTEREDCOMPANY","AIM_REGISTEREDOWNER","AIM_REQUIREDBYPOLICY","AIM_SUPPORTTELEPHONE","AIM_SUPPORTURL","AIM_UPDATEINFOURL","AIM_VERSION","APPINFODATAFLAGS","APPINFODATAFLAGS enumeration [Windows Shell]","inet_APPINFODATAFLAGS","shappmgr/AIM_COMMENTS","shappmgr/AIM_CONTACT","shappmgr/AIM_DISPLAYNAME","shappmgr/AIM_HELPLINK","shappmgr/AIM_IMAGE","shappmgr/AIM_INSTALLDATE","shappmgr/AIM_INSTALLLOCATION","shappmgr/AIM_INSTALLSOURCE","shappmgr/AIM_LANGUAGE","shappmgr/AIM_PRODUCTID","shappmgr/AIM_PUBLISHER","shappmgr/AIM_READMEURL","shappmgr/AIM_REGISTEREDCOMPANY","shappmgr/AIM_REGISTEREDOWNER","shappmgr/AIM_REQUIREDBYPOLICY","shappmgr/AIM_SUPPORTTELEPHONE","shappmgr/AIM_SUPPORTURL","shappmgr/AIM_UPDATEINFOURL","shappmgr/AIM_VERSION","shappmgr/APPINFODATAFLAGS","shell.APPINFODATAFLAGS"]
old-location: shell\APPINFODATAFLAGS.htm
tech.root: shell
ms.assetid: 80cbc46f-9918-4cca-b41b-1b6caa9c26df
ms.date: 12/05/2018
ms.keywords: AIM_COMMENTS, AIM_CONTACT, AIM_DISPLAYNAME, AIM_HELPLINK, AIM_IMAGE, AIM_INSTALLDATE, AIM_INSTALLLOCATION, AIM_INSTALLSOURCE, AIM_LANGUAGE, AIM_PRODUCTID, AIM_PUBLISHER, AIM_READMEURL, AIM_REGISTEREDCOMPANY, AIM_REGISTEREDOWNER, AIM_REQUIREDBYPOLICY, AIM_SUPPORTTELEPHONE, AIM_SUPPORTURL, AIM_UPDATEINFOURL, AIM_VERSION, APPINFODATAFLAGS, APPINFODATAFLAGS enumeration [Windows Shell], inet_APPINFODATAFLAGS, shappmgr/AIM_COMMENTS, shappmgr/AIM_CONTACT, shappmgr/AIM_DISPLAYNAME, shappmgr/AIM_HELPLINK, shappmgr/AIM_IMAGE, shappmgr/AIM_INSTALLDATE, shappmgr/AIM_INSTALLLOCATION, shappmgr/AIM_INSTALLSOURCE, shappmgr/AIM_LANGUAGE, shappmgr/AIM_PRODUCTID, shappmgr/AIM_PUBLISHER, shappmgr/AIM_READMEURL, shappmgr/AIM_REGISTEREDCOMPANY, shappmgr/AIM_REGISTEREDOWNER, shappmgr/AIM_REQUIREDBYPOLICY, shappmgr/AIM_SUPPORTTELEPHONE, shappmgr/AIM_SUPPORTURL, shappmgr/AIM_UPDATEINFOURL, shappmgr/AIM_VERSION, shappmgr/APPINFODATAFLAGS, shell.APPINFODATAFLAGS
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
targetos: Windows
req.typenames: APPINFODATAFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagAppInfoFlags
 - shappmgr/_tagAppInfoFlags
 - APPINFODATAFLAGS
 - shappmgr/APPINFODATAFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shappmgr.h
api_name:
 - APPINFODATAFLAGS
---

# APPINFODATAFLAGS enumeration


## -description

Specifies application information to return from <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getappinfo">IShellApp::GetAppInfo</a>. These flags are bitmasks used in the <a href="/windows/desktop/api/shappmgr/ns-shappmgr-appinfodata">dwMask</a> member of the <b>APPINFODATA</b> structure.

## -enum-fields

### -field AIM_DISPLAYNAME:0x1

Returns the display name.

### -field AIM_VERSION:0x2

Returns the version.

### -field AIM_PUBLISHER:0x4

Returns the application publisher.

### -field AIM_PRODUCTID:0x8

Returns the application's product ID.

### -field AIM_REGISTEREDOWNER:0x10

Returns the application's registered owner.

### -field AIM_REGISTEREDCOMPANY:0x20

Returns the application's registered company.

### -field AIM_LANGUAGE:0x40

Returns the language.

### -field AIM_SUPPORTURL:0x80

Returns the support URL.

### -field AIM_SUPPORTTELEPHONE:0x100

Returns the support telephone number.

### -field AIM_HELPLINK:0x200

Returns the Help link.

### -field AIM_INSTALLLOCATION:0x400

Returns the application's install location.

### -field AIM_INSTALLSOURCE:0x800

Returns the install source.

### -field AIM_INSTALLDATE:0x1000

Returns the application's install date.

### -field AIM_CONTACT:0x4000

Returns the application's contact information.

### -field AIM_COMMENTS:0x8000

Returns application comments.

### -field AIM_IMAGE:0x20000

Returns the application image.

### -field AIM_READMEURL:0x40000

Returns the URL of the application's ReadMe file.

### -field AIM_UPDATEINFOURL:0x80000

Returns the URL of the application's update information.


#### - AIM_REQUIREDBYPOLICY

Obsolete.

## -remarks

Add/Remove Programs in Control Panel uses only <b>AIM_DISPLAYNAME</b> and <b>AIM_SUPPORTURL.</b>
