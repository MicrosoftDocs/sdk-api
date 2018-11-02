---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo
title: ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo
author: windows-sdk-content
description: Retrieves the previous language exception error information object.
old-location: winrt\ilanguageexceptionerrorinfo2_getpreviouslanguageexceptionerrorinfo.htm
tech.root: WinRT
ms.assetid: 10A45EF1-AF8F-498D-B95B-FCE9EF8AB203
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetPreviousLanguageExceptionErrorInfo, GetPreviousLanguageExceptionErrorInfo method [Windows Runtime], GetPreviousLanguageExceptionErrorInfo method [Windows Runtime],ILanguageExceptionErrorInfo2 interface, ILanguageExceptionErrorInfo2 interface [Windows Runtime],GetPreviousLanguageExceptionErrorInfo method, ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo, ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo, restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo, winrt.ilanguageexceptionerrorinfo2_getpreviouslanguageexceptionerrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
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
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionErrorInfo2.GetPreviousLanguageExceptionErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageExceptionErrorInfo2::GetPreviousLanguageExceptionErrorInfo


## -description


Retrieves the previous language exception error information object.


## -parameters




### -param previousLanguageExceptionErrorInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a> object that contains the previous error information object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Generally speaking, <a href="https://msdn.microsoft.com/1E5C74AE-C8C6-4D95-A836-DD47E50CF25D">GetPropagationContextHead</a> is utilized to retrieve the linked list of <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> objects that contains additional error information on the exception in question. You can then use <b>GetPreviousLanguageExceptionErrorInfo</b> to move through that linked list, and examine each error separately.


The operating system also uses this method to retrieve the stored exceptions associated with the error.





## -see-also




<a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a>
 

 

