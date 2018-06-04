---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IProtocolHandlerSite::GetFilter


## -description



        Retrieves the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>according to the supplied parameters.     
        


## -parameters




### -param pclsidObj [in]

Type: <b>CLSID*</b>

Pointer to the CLSID of the document type from the registry. This is used for items with embedded documents to indicate the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>to use for that embedded document.


### -param pcwszContentType [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the type of the document. This is used to retrieve <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a><b>s</b> that are mapped according to MIME type.


### -param pcwszExtension [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the file name extension, without the preceding period. This is used to retrieve <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>objects that are mapped according to the file name extension.


### -param ppFilter [out]

Type: <b>IFilter**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>that the protocol handler uses.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method queries the Filter Host to identify the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>object to use for the URL item.

The choice of filter is based on the file name extension, a CLSID that identifies the file's content type in the registry, or on the MIME content type. You need to provide only one of the three parameters to this method. If you provide multiple parameters, they are tested in the following order: <i>pcwszContentType</i>, <i>pclsidObj</i>, <i>pcwszExtension</i>. The first valid parameter is used to select the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>; the others are ignored.



