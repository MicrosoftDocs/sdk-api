---
UID: NF:propsys.PSPropertyBag_ReadStream
title: PSPropertyBag_ReadStream function (propsys.h)
author: windows-sdk-content
description: Reads the data stream stored in a given property contained in a specified property bag.
old-location: properties\PSPropertyBag_ReadStream.htm
tech.root: properties
ms.assetid: 3D1D8B3E-DD16-4b34-918C-C8478EBF0930
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadStream, PSPropertyBag_ReadStream function [Windows Properties], properties.PSPropertyBag_ReadStream, propsys/PSPropertyBag_ReadStream, shell.PSPropertyBag_ReadStream, shell_PSPropertyBag_ReadStream
ms.topic: function
f1_keywords: 
 - "propsys/PSPropertyBag_ReadStream"
dev_langs:
 - c++
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSPropertyBag_ReadStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_ReadStream function


## -description


Reads the data stream stored in a given property contained in a specified property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object, that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param value [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The address of a pointer that, when this function returns successfully, receives the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller of the <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_readstream">PSPropertyBag_ReadStream</a> function needs to call a <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object returned by this function.



<a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> and <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768194(v=vs.85)">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768195(v=vs.85)">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_writestream">PSPropertyBag_WriteStream</a>
 

 

