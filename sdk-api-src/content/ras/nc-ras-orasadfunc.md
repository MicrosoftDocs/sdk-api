---
UID: NC:ras.ORASADFUNC
title: ORASADFUNC
author: windows-sdk-content
description: The ORASADFunc function is an application-defined callback function that is used to provide a customized user interface for autodialing.
old-location: rras\orasadfunc.htm
old-project: rras
ms.assetid: d3ad49e3-6807-419d-8d05-f703f5327020
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ORASADFunc, ORASADFunc callback, ORASADFunc callback function [RAS], _ras_orasadfunc, ras/ORASADFunc, rras.orasadfunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - ORASADFunc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ORASADFUNC callback function


## -description


The 
<b>ORASADFunc</b> function is an application-defined callback function that is used to provide a customized user interface for autodialing.

This prototype is provided for compatibility with earlier versions of Windows. New applications should use the 
<a href="https://msdn.microsoft.com/e014624a-1ee1-4de3-ba59-cd090b3fa711">RASADFunc</a> callback function. Support for this prototype may be removed in future versions of RAS.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwFlags [in]

Reserved; must be zero.


#### - hwndOwner [in]

Handle of the owner window.


#### - lpdwRetCode [in]

Pointer to a variable that the callback function fills in with the results of the dialing operation. If the dialing operation succeeds, set this variable to ERROR_SUCCESS. If the dialing operation fails, set it to a nonzero value.


#### - lpszEntry [in]

Pointer to a null-terminated string that specifies the phone-book entry to use.


## -returns



If the callback function performs the dialing operation, return <b>TRUE</b>. Use the <i>lpdwRetCode</i> parameter to indicate the results of the dialing operation.

If the callback function does not perform the dialing operation, return <b>FALSE</b>. In this case, the system uses the default user interface for dialing.




## -remarks



If the 
<b>ORASADFunc</b> function performs the dialing operation, it presents its own user interface for dialing and calls the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function to do the actual dialing. The 
<b>ORASADFunc</b> then returns <b>TRUE</b> to indicate that it took over the dialing. When the dialing operation has been completed, set the variable pointed to by <i>lpdwRetCode</i> to indicate success or failure.

To enable an 
<b>ORASADFunc</b> handler for a phone-book entry, use the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure in a call to the 
<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a> function. The <b>szAutodialDll</b> member specifies the name of the DLL that contains the handler, and the <b>szAutodialDll</b> member specifies the exported name of the handler.

The 
<b>ORASADFunc</b> function is a placeholder for the library-defined function name. The <b>ORASADFUNC</b> type is a pointer to an 
<b>ORASADFunc</b> function.




## -see-also




<a href="https://msdn.microsoft.com/e014624a-1ee1-4de3-ba59-cd090b3fa711">RASADFunc</a>



<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

