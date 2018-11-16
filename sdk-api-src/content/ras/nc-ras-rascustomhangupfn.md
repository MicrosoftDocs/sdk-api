---
UID: NC:ras.RasCustomHangUpFn
title: RasCustomHangUpFn
author: windows-sdk-content
description: The RasCustomHangUp function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom connection hang-up routines.
old-location: rras\rascustomhangup.htm
tech.root: RRAS
ms.assetid: 56410af3-7b23-4536-998d-88d78d45585d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RasCustomHangUp, RasCustomHangUp callback function [RAS], RasCustomHangUpFn, RasCustomHangUpFn callback, _ras_rascustomhangup, ras/RasCustomHangUp, rras.rascustomhangup
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasCustomHangUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasCustomHangUpFn callback function


## -description


The 
<b>RasCustomHangUp</b> function is an application-defined function that is exported by a third-party custom-dialing DLL. This function allows third-party vendors to implement custom connection hang-up routines.


## -parameters




### -param hRasConn

Handle to the RAS connection to hang up.


## -returns



If the function succeeds, the return value should be <b>ERROR_SUCCESS</b>.

If the function fails, the return value should be a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



RAS  calls this entry point from 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>, if the <b>szCustomDialDll</b> member of the 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure for the entry being dialed specifies a custom-dialing DLL.




## -see-also




<a href="https://msdn.microsoft.com/ad94f38d-812f-4329-8055-6274a21a3242">Custom Dialers</a>



<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/8c3f807b-3e31-4ce6-8549-74ab06cbba7f">RasCustomDial</a>



<a href="https://msdn.microsoft.com/d1f4715a-a31c-4346-ac0a-83f2c58e8cc1">RasCustomDialDlg</a>



<a href="https://msdn.microsoft.com/4778069b-87d0-4379-95f7-718fe0d7a56c">RasCustomEntryDlg</a>



<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

