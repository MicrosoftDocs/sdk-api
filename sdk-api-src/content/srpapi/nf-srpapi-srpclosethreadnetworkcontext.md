---
UID: NF:srpapi.SrpCloseThreadNetworkContext
title: SrpCloseThreadNetworkContext function
author: windows-sdk-content
description: Restores a thread back to the original context, which may have been optionally returned from SrpCreateThreadNetworkContext.
old-location: edp\srpclosethreadnetworkcontext.htm
tech.root: EDP
ms.assetid: AB8DD527-BABA-40D0-A423-2BEAAA544B2B
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EDP.srpclosethreadnetworkcontext, SrpCloseThreadNetworkContext, SrpCloseThreadNetworkContext function, srpapi/SrpCloseThreadNetworkContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: srpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Srpapi.lib
req.dll: Srpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - srpapi.dll
 - Ext-MS-Win-Security-Srp-L1-1-0.dll
 - Ext-MS-Win-Security-Srp-L1-1-1.dll
api_name:
 - SrpCloseThreadNetworkContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SrpCloseThreadNetworkContext function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Restores a thread back to the original context, which may have been optionally returned from <a href="https://msdn.microsoft.com/95997D25-04FE-445B-ADC1-DE85A34BD70C">SrpCreateThreadNetworkContext</a>. 


## -parameters




### -param threadNetworkContext [in, out]

A handle to the original context’s token.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.



