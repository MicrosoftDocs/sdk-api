---
UID: NF:powrprof.WriteProcessorPwrScheme
title: WriteProcessorPwrScheme function
author: windows-driver-content
description: Writes processor power policy settings for the specified power scheme.
old-location: base\writeprocessorpwrscheme.htm
old-project: Power
ms.assetid: 70e18f50-4774-4a7c-8fe0-7fd6a54aaa90
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WriteProcessorPwrScheme, WriteProcessorPwrScheme function, _win32_writeprocessorpwrscheme, base.writeprocessorpwrscheme, powrprof/WriteProcessorPwrScheme
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PowrProf.dll
api_name:
-	WriteProcessorPwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# WriteProcessorPwrScheme function


## -description


<p class="CCE_Message">[<b>WriteProcessorPwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Writes processor power policy settings for the specified power scheme.


## -parameters




### -param uiID

TBD


### -param pMachineProcessorPowerPolicy [in]

A pointer to a 
<a href="https://msdn.microsoft.com/54403b81-97bc-4f2b-8721-48c9f69e2773">MACHINE_PROCESSOR_POWER_POLICY</a> structure that contains the power policy settings to be written.


#### - ID [in]

The index of the power scheme to be written.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This change does not affect the current system power policy. To apply this change to the current system power policy, call the 
<a href="https://msdn.microsoft.com/f449ff0d-5c22-4c6d-8c88-dc18258a8c6d">SetActivePwrScheme</a> function, using the index of this power scheme.

Starting with Windows Vista, power management configuration of the system's processor is controlled through the GUID_PROCESSOR_SETTINGS_SUBGROUP power settings subgroup. Use the <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> function to enumerate individual settings.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/54403b81-97bc-4f2b-8721-48c9f69e2773">MACHINE_PROCESSOR_POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/740095a7-9def-48a3-9cbb-1da91b052321">ReadProcessorPwrScheme</a>
 

 

