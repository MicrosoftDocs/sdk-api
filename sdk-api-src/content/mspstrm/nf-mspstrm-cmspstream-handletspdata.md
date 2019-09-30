---
UID: NF:mspstrm.CMSPStream.HandleTSPData
title: CMSPStream::HandleTSPData (mspstrm.h)
author: windows-sdk-content
description: The HandleTSPData method may be called by the derived call object to let the stream handle the TSP commands.
old-location: tapi3\cmspstream_handletspdata.htm
tech.root: Tapi
ms.assetid: 2b02690f-9821-488e-b061-916c6338e813
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],HandleTSPData method, CMSPStream.HandleTSPData, CMSPStream::HandleTSPData, HandleTSPData, HandleTSPData method [TAPI 2.2], HandleTSPData method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_handletspdata, mspstrm/CMSPStream::HandleTSPData, tapi3.cmspstream_handletspdata
ms.topic: method
f1_keywords: 
 - "mspstrm/CMSPStream.HandleTSPData"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspstrm.h
api_name:
 - CMSPStream.HandleTSPData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPStream::HandleTSPData


## -description


The 
<b>HandleTSPData</b> method may be called by the derived call object to let the stream handle the TSP commands. The default implementation returns S_OK. Override this method to implement the stream-specific portion of your MSP-TSP communication. Note that the base call object classes do not call this method; if you want to use it, you must also override the 
<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-receivetspcalldata">ReceiveTSPCallData</a> method to dispatch the TSP data to your streams. The stream dispatch information, if any, will be contained in the opaque buffer.


## -parameters




### -param pData

Pointer to opaque buffer containing implementation-dependent information.


### -param dwSize

Size in bytes of opaque buffer.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspstrm/nl-mspstrm-cmspstream">CMSPStream</a>
 

 

