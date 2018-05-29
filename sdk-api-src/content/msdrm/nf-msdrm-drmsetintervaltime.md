---
UID: NF:msdrm.DRMSetIntervalTime
title: DRMSetIntervalTime function
author: windows-sdk-content
description: Specifies the number of days from issuance that can pass before an end&#8211;user license must be renewed.
old-location: rm\drmsetintervaltime.htm
old-project: AdRms_Sdk
ms.assetid: b3b7af75-ed94-4c2f-abb2-95194796771c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMSetIntervalTime, DRMSetIntervalTime function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetIntervalTime, rm.drmsetintervaltime
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMSetIntervalTime
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetIntervalTime function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetIntervalTime</b> function specifies the number of days from issuance that can pass before an end–user license must be renewed. This value is specified in an issuance license.


## -parameters




### -param hIssuanceLicense [in]

The handle of the issuance license in which to  set the interval time.


### -param cDays [in]

An unsigned integer  value that specifies the interval period, in days. For example, if you specify 30, the end–user license must be renewed within 30 days of the day  it was issued.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/681791b1-caeb-46ef-8cae-c93d46a6729e">DRMGetIntervalTime</a>
 

 

