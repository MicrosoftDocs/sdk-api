---
UID: NF:cscobj.IOfflineFilesErrorInfo.GetDescription
title: IOfflineFilesErrorInfo::GetDescription (cscobj.h)
description: Retrieves a text string describing the error.
helpviewer_keywords: ["GetDescription","GetDescription method [Offline Files]","GetDescription method [Offline Files]","IOfflineFilesErrorInfo interface","IOfflineFilesErrorInfo interface [Offline Files]","GetDescription method","IOfflineFilesErrorInfo.GetDescription","IOfflineFilesErrorInfo::GetDescription","cscobj/IOfflineFilesErrorInfo::GetDescription","of.iofflinefileserrorinfo_getdescription"]
old-location: of\iofflinefileserrorinfo_getdescription.htm
tech.root: of
ms.assetid: 04ec70c6-84e0-4543-b49f-1fe058d4d31d
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Offline Files], GetDescription method [Offline Files],IOfflineFilesErrorInfo interface, IOfflineFilesErrorInfo interface [Offline Files],GetDescription method, IOfflineFilesErrorInfo.GetDescription, IOfflineFilesErrorInfo::GetDescription, cscobj/IOfflineFilesErrorInfo::GetDescription, of.iofflinefileserrorinfo_getdescription
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesErrorInfo::GetDescription
 - cscobj/IOfflineFilesErrorInfo::GetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesErrorInfo.GetDescription
---

# IOfflineFilesErrorInfo::GetDescription


## -description

Retrieves a text string describing the error. In most cases, this is the system error string reported for the sync result using the Win32 function <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>.

## -parameters

### -param ppszDescription [out]

Receives the address of a text string describing the error.  The caller must free this memory block by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileserrorinfo">IOfflineFilesErrorInfo</a>