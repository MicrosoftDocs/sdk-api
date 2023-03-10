---
UID: NF:fltuser.FilterClose
title: FilterClose function (fltuser.h)
description: The FilterClose function closes an open minifilter handle.
helpviewer_keywords: ["FilterClose","FilterClose function [Installable File System Drivers]","FltWin32ApiRef_42f7f157-b74a-4856-ac99-bca1caac3493.xml","fltuser/FilterClose","ifsk.filterclose"]
old-location: ifsk\filterclose.htm
tech.root: ifsk
ms.assetid: c5d3774e-6f57-4a6b-97a8-623268884859
ms.date: 12/05/2018
ms.keywords: FilterClose, FilterClose function [Installable File System Drivers], FltWin32ApiRef_42f7f157-b74a-4856-ac99-bca1caac3493.xml, fltuser/FilterClose, ifsk.filterclose
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterClose
 - fltuser/FilterClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterClose
---

# FilterClose function


## -description

The <b>FilterClose</b> function closes an open minifilter handle.

## -parameters

### -param hFilter [in]

Minifilter handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>.

## -returns

<b>FilterClose</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

After <b>FilterClose</b> is called, the minifilter handle that the <i>hFilter</i> parameter specifies is no longer valid and cannot safely be used. 

Use <b>FilterClose</b> to close open minifilter handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>. Use <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a> to close handles returned by calls to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>. 

To close a connection port handle that was opened by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>, use <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -see-also

<a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterconnectcommunicationport">FilterConnectCommunicationPort</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filtercreate">FilterCreate</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindclose">FilterFindClose</a>



<a href="/windows/desktop/api/fltuser/nf-fltuser-filterfindfirst">FilterFindFirst</a>