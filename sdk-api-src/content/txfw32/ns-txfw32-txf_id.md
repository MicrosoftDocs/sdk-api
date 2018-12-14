---
UID: NS:txfw32._TXF_ID
title: TXF_ID
author: windows-sdk-content
description: Represents a unique identifier within the context of the Resource Manager.
old-location: fs\txf_id.htm
tech.root: fileio
ms.assetid: b7bdb226-69ce-4226-b826-baf9c732ec52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTXF_ID, PTXF_ID, PTXF_ID structure pointer [Files], TXF_ID, TXF_ID structure [Files], fs.txf_id, txfw32/PTXF_ID, txfw32/TXF_ID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: txfw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - TxfW32.h
api_name:
 - TXF_ID
product: Windows
targetos: Windows
req.typenames: TXF_ID, *PTXF_ID
req.redist: 
---

# TXF_ID structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Represents a unique identifier within the context of the Resource Manager.


## -struct-fields




### -field LowPart

The low part of the identifier.


### -field HighPart

The high part of the identifier.


## -see-also




<a href="https://msdn.microsoft.com/9fe7375a-58ef-4807-942f-e21858f09217">TXF_LOG_RECORD_AFFECTED_FILE</a>



<a href="https://msdn.microsoft.com/b891f763-13dd-4b40-aff3-3fccb693d76a">TXF_LOG_RECORD_BASE</a>



<a href="https://msdn.microsoft.com/9b6e9be5-39e7-47e3-846f-ea2e5e04597f">TXF_LOG_RECORD_TRUNCATE</a>



<a href="https://msdn.microsoft.com/754ea93e-bc82-498e-8333-eda3262aebc0">TXF_LOG_RECORD_WRITE</a>



<a href="https://msdn.microsoft.com/57218f53-adcd-4a9a-b772-d3dab576b8c1">TxfLogCreateFileReadContext</a>
 

 

