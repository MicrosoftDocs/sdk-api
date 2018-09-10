---
UID: NF:cscobj.IOfflineFilesErrorInfo.GetDescription
title: IOfflineFilesErrorInfo::GetDescription
author: windows-sdk-content
description: Retrieves a text string describing the error.
old-location: of\iofflinefileserrorinfo_getdescription.htm
tech.root: offlinefiles
ms.assetid: 04ec70c6-84e0-4543-b49f-1fe058d4d31d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDescription, GetDescription method [Offline Files], GetDescription method [Offline Files],IOfflineFilesErrorInfo interface, IOfflineFilesErrorInfo interface [Offline Files],GetDescription method, IOfflineFilesErrorInfo.GetDescription, IOfflineFilesErrorInfo::GetDescription, cscobj/IOfflineFilesErrorInfo::GetDescription, of.iofflinefileserrorinfo_getdescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesErrorInfo::GetDescription


## -description


Retrieves a text string describing the error. In most cases, this is the system error string reported for the sync result using the Win32 function <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>.


## -parameters




### -param ppszDescription [out]

Receives the address of a text string describing the error.  The caller must free this memory block by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/6c78d475-aa63-49e4-863f-1a197801f2f9">IOfflineFilesErrorInfo</a>
 

 

