---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo2.GetPropagationContextHead
title: ILanguageExceptionErrorInfo2::GetPropagationContextHead
author: windows-sdk-content
description: Retrieves the propagation context head.
old-location: winrt\ilanguageexceptionerrorinfo2_getpropagationcontexthead.htm
old-project: WinRT
ms.assetid: 1E5C74AE-C8C6-4D95-A836-DD47E50CF25D
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetPropagationContextHead, GetPropagationContextHead method [Windows Runtime], GetPropagationContextHead method [Windows Runtime],ILanguageExceptionErrorInfo2 interface, ILanguageExceptionErrorInfo2 interface [Windows Runtime],GetPropagationContextHead method, ILanguageExceptionErrorInfo2.GetPropagationContextHead, ILanguageExceptionErrorInfo2::GetPropagationContextHead, restrictederrorinfo/ILanguageExceptionErrorInfo2::GetPropagationContextHead, winrt.ilanguageexceptionerrorinfo2_getpropagationcontexthead
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: restrictederrorinfo.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionErrorInfo2.GetPropagationContextHead
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ILanguageExceptionErrorInfo2::GetPropagationContextHead


## -description


Retrieves the propagation context head.


## -parameters




### -param propagatedLanguageExceptionErrorInfoHead [out]

On success, returns an <a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a> object that represents the head of the propagation context.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use <b>GetPropagationContextHead</b> to retrieve the linked list of <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> objects that contains additional error information on the exception in question. You can then use <a href="https://msdn.microsoft.com/10A45EF1-AF8F-498D-B95B-FCE9EF8AB203">GetPreviousLanguageExceptionErrorInfo</a> to move through that linked list, and examine each error separately.

 The operating system also uses this method to retrieve the stored exceptions associated with the error.




## -see-also




<a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a>
 

 

