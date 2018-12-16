---
UID: NF:textstor.ITextStoreACP.RequestAttrsAtPosition
title: ITextStoreACP::RequestAttrsAtPosition
author: windows-sdk-content
description: Gets text attributes at the specified character position.
old-location: tsf\itextstoreacp_requestattrsatposition.htm
tech.root: TSF
ms.assetid: 39eb59cd-ec55-4057-8cf1-0203b6e6c82b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RequestAttrsAtPosition method, ITextStoreACP.RequestAttrsAtPosition, ITextStoreACP::RequestAttrsAtPosition, RequestAttrsAtPosition, RequestAttrsAtPosition method [Text Services Framework], RequestAttrsAtPosition method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_requestattrsatposition_ref, textstor/ITextStoreACP::RequestAttrsAtPosition, tsf.itextstoreacp_requestattrsatposition
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP.RequestAttrsAtPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACP::RequestAttrsAtPosition


## -description


Gets text attributes at the specified character position.


## -parameters




### -param acpPos [in]

Specifies the application character position in the document.


### -param cFilterAttrs [in]

Specifies the number of attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to verify.


### -param dwFlags [in]

Must be zero.


## -returns



This method has no return values.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/6cd34ca5-6561-4161-beac-98248f0415f6">ITextStoreACP::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID
      </a>
 

 

