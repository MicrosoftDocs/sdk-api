---
UID: NF:mspstrm.CMSPStream.HandleTSPData
title: CMSPStream::HandleTSPData
author: windows-sdk-content
description: The HandleTSPData method may be called by the derived call object to let the stream handle the TSP commands.
old-location: tapi3\cmspstream_handletspdata.htm
old-project: Tapi
ms.assetid: 2b02690f-9821-488e-b061-916c6338e813
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CMSPStream interface [TAPI 2.2],HandleTSPData method, CMSPStream.HandleTSPData, CMSPStream::HandleTSPData, HandleTSPData, HandleTSPData method [TAPI 2.2], HandleTSPData method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_handletspdata, mspstrm/CMSPStream::HandleTSPData, tapi3.cmspstream_handletspdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mspstrm.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspstrm.h
api_name:
 - CMSPStream.HandleTSPData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPStream::HandleTSPData


## -description


The 
<b>HandleTSPData</b> method may be called by the derived call object to let the stream handle the TSP commands. The default implementation returns S_OK. Override this method to implement the stream-specific portion of your MSP-TSP communication. Note that the base call object classes do not call this method; if you want to use it, you must also override the 
<a href="https://msdn.microsoft.com/8f5c31cd-7d74-47d4-9e96-8a965843210c">ReceiveTSPCallData</a> method to dispatch the TSP data to your streams. The stream dispatch information, if any, will be contained in the opaque buffer.


## -parameters




### -param pData

Pointer to opaque buffer containing implementation-dependent information.


### -param dwSize

Size in bytes of opaque buffer.


## -see-also




<a href="https://msdn.microsoft.com/776ca663-faa2-4534-8873-4e20ed79530c">CMSPStream</a>
 

 

