---
UID: NF:msdrm.DRMGetIntervalTime
title: DRMGetIntervalTime function
author: windows-sdk-content
description: Retrieves the number of days from issuance that can pass before an end&#8211;user license must be renewed.
old-location: rm\drmgetintervaltime.htm
tech.root: AdRms_Sdk
ms.assetid: 681791b1-caeb-46ef-8cae-c93d46a6729e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMGetIntervalTime, DRMGetIntervalTime function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetIntervalTime, rm.drmgetintervaltime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msdrm.h
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetIntervalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DRMGetIntervalTime
: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetIntervalTime function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetIntervalTime</b> function retrieves the number of days from issuance that can pass before an end–user license must be renewed. This value is retrieved from an issuance license.


## -parameters




### -param hIssuanceLicense [in]

The handle of the issuance license from which the interval time can be retrieved.


### -param pcDays [in]

A pointer to a <b>UINT</b> that specifies the interval period, in days. For example, if the value is  30, the end–user license must be renewed within 30 days of the day  it was issued.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b7af75-ed94-4c2f-abb2-95194796771c">DRMSetIntervalTime</a>
 

 

