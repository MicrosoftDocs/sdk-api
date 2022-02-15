---
UID: NF:msrdc.IRdcSignatureReader.ReadSignatures
title: IRdcSignatureReader::ReadSignatures (msrdc.h)
description: Reads a block of signatures from the current position.
helpviewer_keywords: ["IRdcSignatureReader interface [Remote Differential Compression]","ReadSignatures method","IRdcSignatureReader.ReadSignatures","IRdcSignatureReader::ReadSignatures","ReadSignatures","ReadSignatures method [Remote Differential Compression]","ReadSignatures method [Remote Differential Compression]","IRdcSignatureReader interface","fs.irdcsignaturereader_readsignatures","msrdc/IRdcSignatureReader::ReadSignatures","rdc.irdcsignaturereader_readsignatures"]
old-location: rdc\irdcsignaturereader_readsignatures.htm
tech.root: rdc
ms.assetid: 566a5442-b186-4aac-94fa-5784736a30c3
ms.date: 12/05/2018
ms.keywords: IRdcSignatureReader interface [Remote Differential Compression],ReadSignatures method, IRdcSignatureReader.ReadSignatures, IRdcSignatureReader::ReadSignatures, ReadSignatures, ReadSignatures method [Remote Differential Compression], ReadSignatures method [Remote Differential Compression],IRdcSignatureReader interface, fs.irdcsignaturereader_readsignatures, msrdc/IRdcSignatureReader::ReadSignatures, rdc.irdcsignaturereader_readsignatures
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcSignatureReader::ReadSignatures
 - msrdc/IRdcSignatureReader::ReadSignatures
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcSignatureReader.ReadSignatures
---

# IRdcSignatureReader::ReadSignatures


## -description

The 
   <b>ReadSignatures</b> method
   reads a block of signatures from the current position.

## -parameters

### -param rdcSignaturePointer [in, out]

Address of a <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignaturepointer">RdcSignaturePointer</a> structure. On 
      input the <b>m_Size</b> member of this structure must contain the number of 
      <a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignature">RdcSignature</a> structures in the array pointed to by the 
      <b>m_Data</b> member, and the <b>m_Used</b> member must be zero. On 
      output the <b>m_Used</b> member will contain the number of 
      <b>RdcSignature</b> structures in the array pointed to by the 
      <b>m_Data</b> member.

### -param endOfOutput [out]

Address of a <b>BOOL</b> that is set to <b>TRUE</b> if the end of 
      the signatures has been read.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsignaturereader">IRdcSignatureReader</a>



<a href="/windows/win32/api/msrdc/ns-msrdc-rdcsignaturepointer">RdcSignaturePointer</a>