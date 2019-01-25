---
UID: NF:mspcall.CMSPCallBase.ReceiveTSPCallData
title: CMSPCallBase::ReceiveTSPCallData
author: windows-sdk-content
description: The ReceiveTSPCallData method is called by the MSP address object's ReceiveTSPData method to dispatch TSP data to the correct call.
old-location: tapi3\cmspcallbase_receivetspcalldata.htm
tech.root: Tapi
ms.assetid: 8f5c31cd-7d74-47d4-9e96-8a965843210c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],ReceiveTSPCallData method, CMSPCallBase.ReceiveTSPCallData, CMSPCallBase::ReceiveTSPCallData, ReceiveTSPCallData, ReceiveTSPCallData method [TAPI 2.2], ReceiveTSPCallData method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_receivetspcalldata, mspcall/CMSPCallBase::ReceiveTSPCallData, tapi3.cmspcallbase_receivetspcalldata
ms.topic: method
req.header: mspcall.h
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
 - Mspcall.h
api_name:
 - CMSPCallBase.ReceiveTSPCallData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallBase::ReceiveTSPCallData


## -description


The 
<b>ReceiveTSPCallData</b> method is called by the MSP address object's 
<a href="https://msdn.microsoft.com/80b8e0aa-3361-4593-bec0-cbe9186c6c41">ReceiveTSPData</a> method to dispatch TSP data to the correct call. The call object should override this method to handle the TSP data according to whatever semantics have been defined for communication between this particular MSP and its corresponding TSP. The default implementation simply returns S_OK, which is sufficient for an MSP that does not handle any per-call TSP data.


## -parameters




### -param pBuffer

Pointer to buffer containing TSP data.


### -param dwSize

Size of the buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726496(v=VS.85).aspx">CMSPCallBase</a>
 

 

