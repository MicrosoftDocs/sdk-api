---
UID: NF:tspi.TSPI_lineSetCallData
title: TSPI_lineSetCallData function (tspi.h)
description: The TSPI_lineSetCallData function service provider stores the indicated call data with its information related to the call, and subsequently delivers it whenever TSPI_lineGetCallInfo is called.helpviewer_keywords: ["TSPI_lineSetCallData","TSPI_lineSetCallData function [TAPI 2.2]","_tspi_tspi_linesetcalldata","tspi.tspi_linesetcalldata","tspi/TSPI_lineSetCallData"]
old-location: tspi\tspi_linesetcalldata.htm
tech.root: Tapi
ms.assetid: 0a4b1dba-df2b-4c9e-9a17-4c5f24d152a7
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallData, TSPI_lineSetCallData function [TAPI 2.2], _tspi_tspi_linesetcalldata, tspi.tspi_linesetcalldata, tspi/TSPI_lineSetCallData
f1_keywords:
- tspi/TSPI_lineSetCallData
dev_langs:
- c++
req.header: tspi.h
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
- UserDefined
api_location:
- Tspi.h
api_name:
- TSPI_lineSetCallData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_lineSetCallData function


## -description


The 
<b>TSPI_lineSetCallData</b> function service provider stores the indicated call data with its information related to the call, and subsequently delivers it whenever 
<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a> is called. The service provider sends a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a> message indicating LINECALLINFOSTATE_CALLDATA to show that the call data has changed. Depending on the service provider implementation, the call data can be propagated to all entities having handles to the call, including those on other machines (through the server), and can travel with the call when it is transferred.


## -parameters




### -param dwRequestID

Identifier for reporting asynchronous completion information.


### -param hdCall

The service provider's handle to the call.


### -param lpCallData

Address of the data to be copied to the <b>CallData</b> field in 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, replacing any existing data.


### -param dwSize

Number of bytes of data to be copied. A value of zero causes any existing data to be removed. If the <i>lpCallData</i> parameter is a pointer to a string, the size must include the <b>null</b> terminator. 


## -returns



Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, one of these negative error values:

LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RESOURCEUNAVAIL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)">LINE_CALLINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallinfo">TSPI_lineGetCallInfo</a>
 

 

