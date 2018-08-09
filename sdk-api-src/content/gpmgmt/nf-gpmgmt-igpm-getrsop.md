---
UID: NF:gpmgmt.IGPM.GetRSOP
title: IGPM::GetRSOP
author: windows-sdk-content
description: Creates and returns an GPMRSOP. You can specify the Resultant Set of Policy (RSoP) mode and a Windows Management Instrumentation (WMI) namespace.
old-location: gpmc\igpm_getrsop.htm
old-project: GPMC
ms.assetid: 61a1be3e-d959-47e2-ad6c-ca00accd0afe
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPM object [GPMC],GetRSOP method, GetRSOP, GetRSOP method [GPMC], GetRSOP method [GPMC],GPM object, GetRSOP method [GPMC],IGPM interface, IGPM interface [GPMC],GetRSOP method, IGPM.GetRSOP, IGPM::GetRSOP, _win32_igpm_getrsop, gpmc.igpm_getrsop, gpmgmt/IGPM::GetRSOP, rsopLogging, rsopPlanning, rsopUnknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM.GetRSOP
 - GPM.GetRSOP
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::GetRSOP


## -description


Creates and returns an 
<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">GPMRSOP</a>. You can specify the Resultant Set of Policy (RSoP) mode and a Windows Management Instrumentation (WMI) namespace.


## -parameters




### -param gpmRSoPMode [in]

Required. Mode in which to open the object. The following modes are supported.



#### rsopPlanning

Specifies RSoP planning mode



#### rsopLogging

Specifies RSoP logging mode



#### rsopUnknown

Valid only if the <i>bstrNamespace</i> parameter is specified

To perform the query, RSoP planning mode requires a domain controller that is running Windows Server.


### -param bstrNamespace [in]

WMI namespace for the <a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a><b>GPMRSOP</b><b>GPMRSOP</b>.  Use a null-terminated string. This parameter can be <b>NULL</b>. For more information about how to retrieve the namespace, see the "Remarks" section.


### -param lFlags [in]

This parameter must be zero.


### -param ppIGPMRSOP [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">GPMRSOP</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">GPMRSOP</a> object.




## -remarks



To retrieve the WMI namespace, call the 
<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">Namespace</a> property method of the <a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a> interface. Or, call the <b>RsopCreateSession</b> method of the 
<a href="https://msdn.microsoft.com/c1b5f80b-f5d0-437c-8bde-e3de5b6b8ec7">RsopLoggingModeProvider</a> and 
<a href="https://msdn.microsoft.com/2ced8f97-0200-4495-8163-8ac375bdc053">RsopPlanningModeProvider</a> WMI classes. For more information about these methods, see the <a href="https://msdn.microsoft.com/0e9314f4-bdea-47b1-81a4-9b19b79ac49d">Group Policy</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>
 

 

