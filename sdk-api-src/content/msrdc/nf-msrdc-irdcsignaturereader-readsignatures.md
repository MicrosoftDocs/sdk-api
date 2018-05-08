---
UID: NF:msrdc.IRdcSignatureReader.ReadSignatures
title: IRdcSignatureReader::ReadSignatures
author: windows-driver-content
description: Reads a block of signatures from the current position.
old-location: rdc\irdcsignaturereader_readsignatures.htm
old-project: Rdc
ms.assetid: 566a5442-b186-4aac-94fa-5784736a30c3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IRdcSignatureReader interface [Remote Differential Compression],ReadSignatures method, IRdcSignatureReader.ReadSignatures, IRdcSignatureReader::ReadSignatures, ReadSignatures, ReadSignatures method [Remote Differential Compression], ReadSignatures method [Remote Differential Compression],IRdcSignatureReader interface, fs.irdcsignaturereader_readsignatures, msrdc/IRdcSignatureReader::ReadSignatures, rdc.irdcsignaturereader_readsignatures
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	IRdcSignatureReader.ReadSignatures
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

