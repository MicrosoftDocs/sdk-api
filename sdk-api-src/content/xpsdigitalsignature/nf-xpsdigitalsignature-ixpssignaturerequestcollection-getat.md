---
UID: NF:xpsdigitalsignature.IXpsSignatureRequestCollection.GetAt
title: IXpsSignatureRequestCollection::GetAt (xpsdigitalsignature.h)
author: windows-sdk-content
description: Gets an IXpsSignatureRequest interface pointer from a specified location in the collection.
old-location: xps\ixpssignaturerequestcollection_getat.htm
tech.root: printdocs
ms.assetid: f3bf89d4-468e-4514-a192-165d18fd12e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsSignatureRequestCollection interface, IXpsSignatureRequestCollection interface [XPS Documents and Packaging],GetAt method, IXpsSignatureRequestCollection.GetAt, IXpsSignatureRequestCollection::GetAt, xps.ixpssignaturerequestcollection_getat, xpsdigitalsignature/IXpsSignatureRequestCollection::GetAt
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
 - IXpsSignatureRequestCollection.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureRequestCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer to be obtained.


### -param signatureRequest [out, retval]

The <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="https://msdn.microsoft.com/bb8279e1-a98b-4156-8b90-d9b69411bfa3">IXpsSignatureRequestCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

