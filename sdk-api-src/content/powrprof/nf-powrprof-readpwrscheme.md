---
UID: NF:powrprof.ReadPwrScheme
title: ReadPwrScheme function
author: windows-driver-content
description: Retrieves the power policy settings that are unique to the specified power scheme.
old-location: base\readpwrscheme.htm
old-project: Power
ms.assetid: a8d93820-b652-4358-8039-8987fac95dca
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ReadPwrScheme, ReadPwrScheme function, _win32_readpwrscheme, base.readpwrscheme, powrprof/ReadPwrScheme
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
-	ReadPwrScheme
product: Windows
targetos: Windows
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ReadPwrScheme function


## -description


<p class="CCE_Message">[<b>ReadPwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. See Remarks.]

Retrieves the power policy settings that are unique to the specified power scheme.


## -parameters




### -param uiID [in]

The index of the power scheme to be read.


### -param pPowerPolicy [out]

A pointer to a 
<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a> structure that receives the power policy settings.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the power scheme specified does not exist, the function returns <b>FALSE</b>.

To retrieve information about the power policy settings currently in use by the system, call the 
<a href="https://msdn.microsoft.com/2a321372-40ff-4292-8b66-db3f794e5f53">GetActivePwrScheme</a> function. To retrieve additional information about the current power policy settings, call the 
<a href="https://msdn.microsoft.com/adc0052d-e2dd-4c55-996c-6af8f5987d79">CallNtPowerInformation</a> function.

Starting with Windows Vista, use the <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> function to enumerate power settings for a specified scheme and the power read functions to retrieve individual settings. 

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a321372-40ff-4292-8b66-db3f794e5f53">GetActivePwrScheme</a>



<a href="https://msdn.microsoft.com/ba49fca6-04b6-4627-a653-07c3fc0dab22">POWER_POLICY</a>



<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a>
 

 

