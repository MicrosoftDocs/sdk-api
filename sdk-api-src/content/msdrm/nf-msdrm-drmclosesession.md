---
UID: NF:msdrm.DRMCloseSession
title: DRMCloseSession function
author: windows-driver-content
description: Closes a client session or a license storage session.
old-location: rm\drmclosesession.htm
old-project: AdRms_Sdk
ms.assetid: e948b31f-382c-4a32-8cc3-98df8c4a6db0
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMCloseSession, DRMCloseSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCloseSession, rm.drmclosesession
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	DRMCloseSession
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2  or later
---

# DRMCloseSession function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCloseSession</b> function closes a client session or a license storage session.


## -parameters




### -param hSession [in]

A handle to the session to be closed.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Client sessions are created by using the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function. License storage sessions are created by using the <a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a> function. Be sure to close a session properly by using this function, which clears out sensitive information from memory and properly closes session handles.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/f6980a9b-9e3c-47e4-b1c3-7e244ca77e44">Activating a Computer</a>



<a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a>



<a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a>
 

 

