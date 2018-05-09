---
UID: NF:ntlsa.LsaGetAppliedCAPIDs
title: LsaGetAppliedCAPIDs function
author: windows-driver-content
description: Returns an array of central access policies (CAPs) identifiers (CAPIDs) of all the CAPs applied on a specific computer.
old-location: security\lsagetappliedcapids.htm
old-project: SecAuthN
ms.assetid: DF10F5CE-BBF5-4CA8-919B-F59B7775C983
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: LsaGetAppliedCAPIDs, LsaGetAppliedCAPIDs function [Security], ntlsa/LsaGetAppliedCAPIDs, security.lsagetappliedcapids
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntlsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VBS_ENCLAVE_REPORT_VARDATA_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LsaGetAppliedCAPIDs
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LsaGetAppliedCAPIDs function


## -description


The <b>LsaGetAppliedCAPIDs</b> function returns an array of central access policies (CAPs) identifiers (CAPIDs) of all the CAPs applied on a specific computer.


## -parameters




### -param SystemName [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the specific computer. The name can have the form of "ComputerName" or "\\ComputerName". If this parameter is <b>NULL</b>, then the function returns the CAPIDs of the local computer.


### -param CAPIDs [out]

A pointer to a variable that receives an array of pointers to CAPIDs that identify the CAPs available on the specified computer. When you have finished using the CAPIDs, call the <a href="https://msdn.microsoft.com/6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9">LsaFreeMemory</a> function on each element in the array and the entire array.


### -param CAPIDCount [out]

A pointer to a variable that receives the number of CAPs that are available on the specified computer. The array returned in the <i>CAPIDs</i> parameter contains the same number of elements as the <i>CAPIDCount</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is one of the <a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>. You can use the <a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to  convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



For specific details about the central access policies, you can query the attributes of the central access policy object in the Active Directory on the specified computer's domain controller.  Look for the object whose <b>msAuthz-CentralAccessPolicyID</b> attribute matches one of the returned CAPIDs. 




## -see-also




<a href="https://msdn.microsoft.com/5A06B8D8-F14B-4D9E-9ED6-4246A26BF945">Centralized Authorization Policy</a>
 

 

