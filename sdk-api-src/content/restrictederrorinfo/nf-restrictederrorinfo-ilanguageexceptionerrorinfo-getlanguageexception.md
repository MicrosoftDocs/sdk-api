---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo.GetLanguageException
title: ILanguageExceptionErrorInfo::GetLanguageException (restrictederrorinfo.h)
author: windows-sdk-content
description: Gets the stored IUnknown object from the error object.
old-location: winrt\ilanguageexceptionerrorinfo_getlanguageexception.htm
tech.root: WinRT
ms.assetid: 94B34741-88AA-4AD4-B1F4-30A7AE5AFCC8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLanguageException, GetLanguageException method [Windows Runtime], GetLanguageException method [Windows Runtime],ILanguageExceptionErrorInfo interface, ILanguageExceptionErrorInfo interface [Windows Runtime],GetLanguageException method, ILanguageExceptionErrorInfo.GetLanguageException, ILanguageExceptionErrorInfo::GetLanguageException, restrictederrorinfo/ILanguageExceptionErrorInfo::GetLanguageException, winrt.ilanguageexceptionerrorinfo_getlanguageexception
ms.topic: method
f1_keywords: ["restrictederrorinfo/ILanguageExceptionErrorInfo.GetLanguageException"]
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
 - ILanguageExceptionErrorInfo.GetLanguageException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILanguageExceptionErrorInfo::GetLanguageException


## -description


Gets the stored <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> object from the error object.


## -parameters




### -param languageException [out]

The stored <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> object from the error object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Language projections query for the appropriate interface to identify this object as generated from an exception to get the original object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo">ILanguageExceptionErrorInfo</a>
 

 

