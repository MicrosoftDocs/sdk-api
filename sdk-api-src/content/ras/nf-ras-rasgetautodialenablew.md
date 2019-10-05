---
UID: NF:ras.RasGetAutodialEnableW
title: RasGetAutodialEnableW function (ras.h)
author: windows-sdk-content
description: The RasGetAutodialEnable function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location.
old-location: rras\rasgetautodialenable.htm
tech.root: RRAS
ms.assetid: 221f91e6-86bd-4450-92c8-ec3290712c18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RasGetAutodialEnable, RasGetAutodialEnable function [RAS], RasGetAutodialEnableA, RasGetAutodialEnableW, _ras_rasgetautodialenable, ras/RasGetAutodialEnable, ras/RasGetAutodialEnableA, ras/RasGetAutodialEnableW, rras.rasgetautodialenable
ms.topic: function
f1_keywords: 
 - "ras/RasGetAutodialEnable"
dev_langs:
 - c++
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
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasGetAutodialEnableW function


## -description


The 
<b>RasGetAutodialEnable</b> function indicates whether the AutoDial feature is enabled for a specified TAPI dialing location. For more information about TAPI dialing locations, see the <a href="https://docs.microsoft.com/windows/desktop/Tapi/telephony-application-programming-interfaces">TAPI Programmer's Reference</a> in the Platform Software Development Kit (SDK).


## -parameters




### -param arg1 [in]

Specifies the identifier of a TAPI dialing location.


### -param arg2 [out]

Pointer to a BOOL variable that receives a nonzero value if AutoDial is enabled for the specified dialing location, or zero if it is not enabled.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is from <a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rassetautodialenablea">RasSetAutodialEnable</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

