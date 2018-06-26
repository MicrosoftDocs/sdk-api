---
UID: NF:ras.RasGetAutodialEnableA
title: RasGetAutodialEnableA function
author: windows-sdk-content
description: The RasGetAutodialEnable function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location.
old-location: rras\rasgetautodialenable.htm
old-project: RRAS
ms.assetid: 221f91e6-86bd-4450-92c8-ec3290712c18
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: RasGetAutodialEnable, RasGetAutodialEnable function [RAS], RasGetAutodialEnableA, RasGetAutodialEnableW, _ras_rasgetautodialenable, ras/RasGetAutodialEnable, ras/RasGetAutodialEnableA, ras/RasGetAutodialEnableW, rras.rasgetautodialenable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetAutodialEnableW (Unicode) and RasGetAutodialEnableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasGetAutodialEnable
 - RasGetAutodialEnableA
 - RasGetAutodialEnableW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasGetAutodialEnableA function


## -description


The 
<b>RasGetAutodialEnable</b> function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location. For more information about TAPI dialing locations, see the <a href="https://msdn.microsoft.com/e7348296-ee2d-4e0a-b274-3563dccea841">TAPI Programmer's Reference</a> in the Platform Software Development Kit (SDK).


## -parameters




### -param

TBD




#### - dwDialingLocation [in]

Specifies the identifier of a TAPI dialing location.


#### - lpfEnabled [out]

Pointer to a BOOL variable that receives a nonzero value if AutoDial is enabled for the specified dialing location, or zero if it is not enabled.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/0d5f7b8e-9bce-4e72-8657-f465ce4008c4">RasSetAutodialEnable</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

