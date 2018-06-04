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

# IRdcSignatureReader::ReadSignatures


## -description


The 
   <b>ReadSignatures</b> method
   reads a block of signatures from the current position.


## -parameters




### -param rdcSignaturePointer [in, out]

Address of a <a href="https://msdn.microsoft.com/ece0fddf-1c06-493d-aed9-6bc86bb014f3">RdcSignaturePointer</a> structure. On 
      input the <b>m_Size</b> member of this structure must contain the number of 
      <a href="https://msdn.microsoft.com/eca15d66-1d8c-422b-a2ab-7dbe00cb4087">RdcSignature</a> structures in the array pointed to by the 
      <b>m_Data</b> member, and the <b>m_Used</b> member must be zero. On 
      output the <b>m_Used</b> member will contain the number of 
      <b>RdcSignature</b> structures in the array pointed to by the 
      <b>m_Data</b> member.


### -param endOfOutput [out]

Address of a <b>BOOL</b> that is set to <b>TRUE</b> if the end of 
      the signatures has been read.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dec6eb10-1243-4888-9ccc-ab1f4cfb11e7">IRdcSignatureReader</a>



<a href="https://msdn.microsoft.com/ece0fddf-1c06-493d-aed9-6bc86bb014f3">RdcSignaturePointer</a>
 

 

