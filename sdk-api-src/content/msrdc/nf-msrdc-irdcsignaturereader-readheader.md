---
UID: NF:msrdc.IRdcSignatureReader.ReadHeader
title: IRdcSignatureReader::ReadHeader
author: windows-sdk-content
description: Reads the signature header and returns a copy of the parameters used to generate the signatures.
old-location: rdc\irdcsignaturereader_readheader.htm
old-project: Rdc
ms.assetid: c0f4d31d-338f-49fc-9f1a-e8e31ffa1bc7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcSignatureReader interface [Remote Differential Compression],ReadHeader method, IRdcSignatureReader.ReadHeader, IRdcSignatureReader::ReadHeader, ReadHeader, ReadHeader method [Remote Differential Compression], ReadHeader method [Remote Differential Compression],IRdcSignatureReader interface, fs.irdcsignaturereader_readheader, msrdc/IRdcSignatureReader::ReadHeader, rdc.irdcsignaturereader_readheader
ms.prod: windows
ms.technology: windows-sdk
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
-	IRdcSignatureReader.ReadHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcSignatureReader::ReadHeader


## -description


The 
   <b>ReadHeader</b> method
   reads the signature header and returns a copy of the parameters
   used to generate the signatures.


## -parameters




### -param rdc_ErrorCode [out]

Address of a <a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a> enumeration that will 
      receive any RDC-specific error code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dec6eb10-1243-4888-9ccc-ab1f4cfb11e7">IRdcSignatureReader</a>



<a href="https://msdn.microsoft.com/32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be">RDC_ErrorCode</a>
 

 

