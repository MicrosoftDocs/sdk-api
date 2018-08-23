---
UID: NF:ras.RasSetAutodialEnableW
title: RasSetAutodialEnableW function
author: windows-sdk-content
description: The RasSetAutodialEnable function enables or disables the AutoDial feature for a specified TAPI dialing location.
old-location: rras\rassetautodialenable.htm
old-project: rras
ms.assetid: 0d5f7b8e-9bce-4e72-8657-f465ce4008c4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasSetAutodialEnable, RasSetAutodialEnable function [RAS], RasSetAutodialEnableA, RasSetAutodialEnableW, _ras_rassetautodialenable, ras/RasSetAutodialEnable, ras/RasSetAutodialEnableA, ras/RasSetAutodialEnableW, rras.rassetautodialenable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetAutodialEnableW (Unicode) and RasSetAutodialEnableA (ANSI)
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
 - RasSetAutodialEnable
 - RasSetAutodialEnableA
 - RasSetAutodialEnableW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasSetAutodialEnableW function


## -description


The 
<b>RasSetAutodialEnable</b> function enables or disables the AutoDial feature for a specified TAPI dialing location. For more information about TAPI dialing locations, see  <a href="_tapi3_telephony_application_programming_interfaces">Telephony Application Programming Interfaces (TAPI)</a>  in the Platform Software Development Kit (SDK).


## -parameters




### -param

TBD




#### - [in]

Specifies the identifier of a TAPI dialing location.


#### - fEnabled [in]

Specifies <b>TRUE</b> to enable AutoDial for the dialing location indicated by the <i>dwDialingLocation</i> parameter. Specifies <b>FALSE</b> to disable it.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a non-zero error code from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/221f91e6-86bd-4450-92c8-ec3290712c18">RasGetAutodialEnable</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

