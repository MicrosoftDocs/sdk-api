---
UID: NE:shappmgr._tagPublishedAppInfoFlags
title: PUBAPPINFOFLAGS (shappmgr.h)
description: Specifies which members in the PUBAPPINFO structure are valid. These flags are bitmasks set in the dwMask member and passed to IPublishedApp::GetPublishedAppInfo.
helpviewer_keywords: ["PAI_ASSIGNEDTIME","PAI_EXPIRETIME","PAI_PUBLISHEDTIME","PAI_SCHEDULEDTIME","PAI_SOURCE","PUBAPPINFOFLAGS","PUBAPPINFOFLAGS enumeration [Windows Shell]","inet_PUBAPPINFOFLAGS","shappmgr/PAI_ASSIGNEDTIME","shappmgr/PAI_EXPIRETIME","shappmgr/PAI_PUBLISHEDTIME","shappmgr/PAI_SCHEDULEDTIME","shappmgr/PAI_SOURCE","shappmgr/PUBAPPINFOFLAGS","shell.PUBAPPINFOFLAGS"]
old-location: shell\PUBAPPINFOFLAGS.htm
tech.root: shell
ms.assetid: 9fcb93a5-24b5-4bc3-9f20-0088affb183b
ms.date: 12/05/2018
ms.keywords: PAI_ASSIGNEDTIME, PAI_EXPIRETIME, PAI_PUBLISHEDTIME, PAI_SCHEDULEDTIME, PAI_SOURCE, PUBAPPINFOFLAGS, PUBAPPINFOFLAGS enumeration [Windows Shell], inet_PUBAPPINFOFLAGS, shappmgr/PAI_ASSIGNEDTIME, shappmgr/PAI_EXPIRETIME, shappmgr/PAI_PUBLISHEDTIME, shappmgr/PAI_SCHEDULEDTIME, shappmgr/PAI_SOURCE, shappmgr/PUBAPPINFOFLAGS, shell.PUBAPPINFOFLAGS
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
req.typenames: PUBAPPINFOFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagPublishedAppInfoFlags
 - shappmgr/_tagPublishedAppInfoFlags
 - PUBAPPINFOFLAGS
 - shappmgr/PUBAPPINFOFLAGS
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
 - PUBAPPINFOFLAGS
---

# PUBAPPINFOFLAGS enumeration


## -description

Specifies which members in the <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">PUBAPPINFO</a> structure are valid. These flags are bitmasks set in the <b>dwMask</b> member and passed to <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">IPublishedApp::GetPublishedAppInfo</a>.

## -enum-fields

### -field PAI_SOURCE:0x1

The <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">pszSource</a> string is valid and contains the display name of the publishing source. If multiple sources publish an application of the same name, Add/Remove Programs identifies them by "&lt;application name&gt; : &lt;publishing source&gt;".

### -field PAI_ASSIGNEDTIME:0x2

The <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">stAssigned</a> member is valid and contains the time that the application should be installed as assigned by an application administrator.

### -field PAI_PUBLISHEDTIME:0x4

Not used.

### -field PAI_SCHEDULEDTIME:0x8

The <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">stScheduled</a> member is valid and contains the time that the application should be installed as assigned by the user.

### -field PAI_EXPIRETIME:0x10

The <a href="/windows/desktop/api/shappmgr/ns-shappmgr-pubappinfo">stExpired</a> member is valid and contains the time after which Add/Remove Programs should no longer install the program.

## -see-also

<a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">IPublishedApp::GetPublishedAppInfo</a>
