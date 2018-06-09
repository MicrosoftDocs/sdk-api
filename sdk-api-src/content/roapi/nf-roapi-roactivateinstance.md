---
UID: NF:roapi.RoActivateInstance
title: RoActivateInstance function
author: windows-sdk-content
description: Activates the specified Windows Runtime class.
old-location: winrt\roactivateinstance.htm
old-project: WinRT
ms.assetid: 20E469FE-100B-489F-956A-347716FA8A12
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: RoActivateInstance, RoActivateInstance function [Windows Runtime], WinRTActivateInstance, roapi/RoActivateInstance, roapi/WinRTActivateInstance, winrt.roactivateinstance, winrt.winrtactivateinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: RO_INIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roapi.h
 - API-MS-Win-Core-WinRT-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoActivateInstance
 - WinRTActivateInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RoActivateInstance function


## -description


Activates the specified Windows Runtime class.


## -parameters




### -param activatableClassId [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The class identifier that is associated with the activatable runtime class.


### -param instance [out]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to the activated instance of the runtime class.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The class was activated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>instance</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The thread has not been initialized in the Windows Runtime by calling the <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/75E30E4B-EE5F-41C4-AC22-91D542E920EB">TrustLevel</a> for the class requires a full-trust process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface is not implemented by the specified class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to create an instance of the class.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoActivateInstance</b> function to activate a Windows Runtime class. The <b>RoActivateInstance</b> function connects to the activation factory that is associated with the specified activatable class identifier, creates an instance by calling the zero-argument constructor on the class, and releases the activation factory.




## -see-also




<a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/C6A2ED6E-9C45-4CF3-A301-72A5DAEB4DFC">IActivationFactory</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/75E30E4B-EE5F-41C4-AC22-91D542E920EB">TrustLevel</a>
 

 

