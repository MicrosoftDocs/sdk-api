---
UID: NF:xpsdigitalsignature.IXpsSignatureCollection.GetAt
title: IXpsSignatureCollection::GetAt (xpsdigitalsignature.h)
author: windows-sdk-content
description: Gets an IXpsSignature interface pointer from a specified location in the collection.
old-location: xps\ixpssignaturecollection_getat.htm
tech.root: printdocs
ms.assetid: 90e9f68b-2f26-481d-8e5e-1ce0409451cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsSignatureCollection interface, IXpsSignatureCollection interface [XPS Documents and Packaging],GetAt method, IXpsSignatureCollection.GetAt, IXpsSignatureCollection::GetAt, xps.ixpssignaturecollection_getat, xpsdigitalsignature/IXpsSignatureCollection::GetAt
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
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
 - xpsdigitalsignature.h
api_name:
 - IXpsSignatureCollection.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface pointer to be obtained.


### -param signature [out, retval]

The <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

