---
UID: NS:shappmgr._PubAppInfo
title: PUBAPPINFO (shappmgr.h)
description: Provides information about a published application from an application publisher to Add/Remove Programs in Control Panel.
helpviewer_keywords: ["*PPUBAPPINFO","PUBAPPINFO","PUBAPPINFO structure [Windows Shell]","inet_PUBAPPINFO","shappmgr/PUBAPPINFO","shell.PUBAPPINFO"]
old-location: shell\PUBAPPINFO.htm
tech.root: shell
ms.assetid: 927c58d3-4208-4fd3-a3fa-18ae7d8d3136
ms.date: 12/05/2018
ms.keywords: '*PPUBAPPINFO, PUBAPPINFO, PUBAPPINFO structure [Windows Shell], inet_PUBAPPINFO, shappmgr/PUBAPPINFO, shell.PUBAPPINFO'
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
req.typenames: PUBAPPINFO, *PPUBAPPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PubAppInfo
 - shappmgr/_PubAppInfo
 - PPUBAPPINFO
 - shappmgr/PPUBAPPINFO
 - PUBAPPINFO
 - shappmgr/PUBAPPINFO
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
 - PUBAPPINFO
---

# PUBAPPINFO structure


## -description

Provides information about a published application from an application publisher to <b>Add/Remove Programs</b> in Control Panel.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the size of the structure. This member is set by the <b>Add/Remove Programs</b> utility.

### -field dwMask

Type: <b>DWORD</b>

A bitmask that indicates which items in the structure are valid. This member can contain one or more <a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags">PUBAPPINFOFLAGS</a>.

### -field pszSource

Type: <b>LPWSTR</b>

A pointer to a string containing the display name of the publisher. This name appears in <b>Add/Remove Programs</b> if duplicate application names are encountered. The string buffer must be allocated using the Shell task allocator.

### -field stAssigned

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

The time when an application manager schedules the application installation.  <b>Add/Remove Programs</b> does not allow the user to schedule an installation time later than the value in this member. This member is ignored if it describes a time prior to the current time.

### -field stPublished

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

### -field stScheduled

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

The installation time that the user sets by clicking <b>Add Later</b>. <b>Add/Remove Programs</b> calls the <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-install">IPublishedApp::Install</a> method with the <i>pInstallTime</i> parameter pointing to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time the user entered. The application publisher maintains this value for installation scheduling. <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo">IPublishedApp::GetPublishedAppInfo</a> returns the scheduled installation time in this member if the scheduled time has not been canceled using <a href="/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp-unschedule">IPublishedApp::Unschedule</a>.

### -field stExpire

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

The time after which you cannot install the published application using <b>Add/Remove Programs</b>.

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>