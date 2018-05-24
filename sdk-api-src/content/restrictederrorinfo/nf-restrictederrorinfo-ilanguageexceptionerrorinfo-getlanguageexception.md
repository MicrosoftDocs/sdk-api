---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo.GetLanguageException
title: ILanguageExceptionErrorInfo::GetLanguageException
author: windows-driver-content
description: Gets the stored IUnknown object from the error object.
old-location: winrt\ilanguageexceptionerrorinfo_getlanguageexception.htm
old-project: WinRT
ms.assetid: 94B34741-88AA-4AD4-B1F4-30A7AE5AFCC8
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: GetLanguageException, GetLanguageException method [Windows Runtime], GetLanguageException method [Windows Runtime],ILanguageExceptionErrorInfo interface, ILanguageExceptionErrorInfo interface [Windows Runtime],GetLanguageException method, ILanguageExceptionErrorInfo.GetLanguageException, ILanguageExceptionErrorInfo::GetLanguageException, restrictederrorinfo/ILanguageExceptionErrorInfo::GetLanguageException, winrt.ilanguageexceptionerrorinfo_getlanguageexception
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
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
req.typenames: RM_UNIQUE_PROCESS, *PRM_UNIQUE_PROCESS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	restrictederrorinfo.h
api_name:
-	ILanguageExceptionErrorInfo.GetLanguageException
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ILanguageExceptionErrorInfo::GetLanguageException


## -description


Gets the stored <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> object from the error object.


## -parameters




### -param languageException [out]

The stored <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> object from the error object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Language projections query for the appropriate interface to identify this object as generated from an exception to get the original object.




## -see-also




<a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>
 

 

