---
UID: NF:msdrm.DRMRepair
title: DRMRepair function
author: windows-sdk-content
description: Repairs a client machine by deleting certificates previously created for the machine or user.
old-location: rm\drmrepair.htm
old-project: AdRms_Sdk
ms.assetid: d3abebcd-1200-417c-a0ec-64768b3c320a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMRepair, DRMRepair function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMRepair, rm.drmrepair
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMRepair
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMRepair function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMRepair</b> function repairs a client machine by deleting certificates previously created for the machine or user.


## -parameters






## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>DRMRepair</b> function first determines whether the machine is activated. If the machine activation is not valid, then the <b>DRMRepair</b> function will restore the machine to a clean state by deleting the machine certificate, rights account certificate, and client licensor certificate of the  currently logged on user.

If the machine activation is valid but the rights account certificate is not valid, then the <b>DRMRepair</b> function will delete the rights account certificate and client licensor certificate of the  currently logged on user.




## -see-also




<a href="https://msdn.microsoft.com/fff0d503-e342-4f50-810c-bda4e9e14ad7">DRMSetGlobalOptions</a>
 

 

