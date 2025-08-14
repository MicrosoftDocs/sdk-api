---
UID: NF:evntcons.EventAccessRemove
title: EventAccessRemove function (evntcons.h)
description: Removes the permissions defined in the registry for the specified provider or session.
helpviewer_keywords: ["EventAccessRemove","EventAccessRemove function [ETW]","base.eventaccessremove_func","etw.eventaccessremove_func","evntcons/EventAccessRemove"]
old-location: etw\eventaccessremove_func.htm
tech.root: ETW
ms.assetid: 9f25f163-046c-41b0-82f9-0b214b74b87e
ms.date: 12/05/2018
ms.keywords: EventAccessRemove, EventAccessRemove function [ETW], base.eventaccessremove_func, etw.eventaccessremove_func, evntcons/EventAccessRemove
req.header: evntcons.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventAccessRemove
 - evntcons/EventAccessRemove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
 - EventAccessRemove
---

# EventAccessRemove function (evntcons.h)


## -description

Removes the permissions defined in the registry for the specified provider or session.

## -parameters

### -param Guid [in]

GUID that uniquely identifies the provider or session whose permissions you want to remove from the 
      registry.

## -returns

Returns ERROR_SUCCESS if successful.

## -remarks

After removing the permission from the registry, the default permissions apply to the provider or session. For 
    details on the default permissions, see 
    <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>.

## -see-also

<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>



<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccessquery">EventAccessQuery</a>