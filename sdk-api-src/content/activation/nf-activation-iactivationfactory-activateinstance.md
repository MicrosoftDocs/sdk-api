---
UID: NF:activation.IActivationFactory.ActivateInstance
title: IActivationFactory::ActivateInstance
author: windows-sdk-content
description: Creates a new instance of the Windows Runtime class that is associated with the current activation factory.
old-location: winrt\iactivationfactory_activateinstance.htm
old-project: WinRT
ms.assetid: AE3E2D87-3AE7-42C3-AA1D-510E717D2E51
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: ActivateInstance, ActivateInstance method [Windows Runtime], ActivateInstance method [Windows Runtime],IActivationFactory interface, IActivationFactory interface [Windows Runtime],ActivateInstance method, IActivationFactory.ActivateInstance, IActivationFactory::ActivateInstance, activation/IActivationFactory::ActivateInstance, winrt.iactivationfactory_activateinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: activation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SI_OBJECT_INFO, *PSI_OBJECT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activation.h
api_name:
-	IActivationFactory.ActivateInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IActivationFactory::ActivateInstance


## -description


Creates a new instance of the Windows Runtime class that is associated with the current activation factory.


## -parameters




### -param instance [out]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new instance of the class that is associated with the current activation factory.


## -returns



Type: <b>HRESULT</b>

This function can return the following values.

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
The  new class instance was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>instance</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface is not implemented by the class that is associated with the current activation factory.

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



Use the <b>ActivateInstance</b> function to activate a Windows Runtime class. The <b>ActivateInstance</b> function connects to the activation factory that is associated with the specified activatable class identifier, creates an instance by calling the zero-argument constructor on the class, and releases the activation factory.




## -see-also




<a href="https://msdn.microsoft.com/C6A2ED6E-9C45-4CF3-A301-72A5DAEB4DFC">IActivationFactory</a>



<a href="https://msdn.microsoft.com/20E469FE-100B-489F-956A-347716FA8A12">RoActivateInstance</a>
 

 

