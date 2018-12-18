---
UID: NF:ras.RasUpdateConnection
title: RasUpdateConnection function
author: windows-sdk-content
description: The RasUpdateConnection function updates the tunnel endpoints of an Internet Key Exchange version 2 (IKEv2) connection.
old-location: rras\rasupdateconnection.htm
tech.root: rras
ms.assetid: ab4fd68c-acc0-4586-9d3d-b796e23d635d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RasUpdateConnection, RasUpdateConnection function [RAS], ras/RasUpdateConnection, rras.rasupdateconnection
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - RasUpdateConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasUpdateConnection function


## -description


The 
<b>RasUpdateConnection</b> function updates the tunnel endpoints of an Internet Key Exchange version 2 (IKEv2) connection.


## -parameters




### -param hrasconn [in]

A handle to the IKEv2 RAS connection for which the tunnel endpoints are to be changed. This can be a handle returned by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> function.


### -param lprasupdateconn [in]

A pointer to a <a href="https://msdn.microsoft.com/eb665afb-2ffd-484b-b7b6-04a92879c98c">RASUPDATECONN</a> structure that contains the new tunnel endpoints  for the RAS connection specified by <i>hrasconn</i>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the error codes from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



Note that 32-bit applications that call <b>RasUpdateConnection</b> will fail when run on a 64-bit machine. The workaround is to write a 64-bit version of the application for 64-bit machines.




## -see-also




<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

