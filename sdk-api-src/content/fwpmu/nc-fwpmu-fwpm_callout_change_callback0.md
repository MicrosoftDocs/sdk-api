---
UID: NC:fwpmu.FWPM_CALLOUT_CHANGE_CALLBACK0
title: FWPM_CALLOUT_CHANGE_CALLBACK0
author: windows-sdk-content
description: Is used to add custom behavior to the callout change notification process.
old-location: fwp\fwpm_callout_change_callback0_func.htm
tech.root: fwp
ms.assetid: 82c678a5-adba-42ea-b85c-4bbdcec78673
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_CALLOUT_CHANGE_CALLBACK0, FWPM_CALLOUT_CHANGE_CALLBACK0 callback, FWPM_CALLOUT_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_callout_change_callback0_func, fwpmu/FWPM_CALLOUT_CHANGE_CALLBACK0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_CALLOUT_CHANGE_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FWPM_CALLOUT_CHANGE_CALLBACK0 callback function


## -description


The <b>FWPM_CALLOUT_CHANGE_CALLBACK0</b> function is used to add custom behavior to the callout change notification process.


## -parameters




### -param *context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/1460603c-6897-4559-b376-b87a6c2f4309">FwpmCalloutSubscribeChanges0</a> function.


### -param *change [in]

Type: <b>const <a href="https://msdn.microsoft.com/70e2eaae-dd75-4acc-87fb-ab2ad450a234">FWPM_CALLOUT_CHANGE0</a>*</b>

The change notification information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/1460603c-6897-4559-b376-b87a6c2f4309">FwpmCalloutSubscribeChanges0</a> to register this callback function.

<b>FWPM_CALLOUT_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_CALLOUT_CHANGE_CALLBACK. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/70e2eaae-dd75-4acc-87fb-ab2ad450a234">FWPM_CALLOUT_CHANGE0</a>



<a href="https://msdn.microsoft.com/1460603c-6897-4559-b376-b87a6c2f4309">FwpmCalloutSubscribeChanges0</a>
 

 

