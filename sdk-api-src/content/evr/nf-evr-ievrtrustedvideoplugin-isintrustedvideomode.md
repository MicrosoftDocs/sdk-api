---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IEVRTrustedVideoPlugin::IsInTrustedVideoMode


## -description



          Queries whether the plug-in has any transient vulnerabilities at this time.
        


## -parameters




### -param pYes [out]

Receives a Boolean value. If <b>TRUE</b>, the plug-in has no transient vulnerabilities at the moment and can receive protected content. If <b>FALSE</b>, the plug-in has a transient vulnerability. If the method fails, the EVR treats the value as <b>FALSE</b> (untrusted).


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method provides a way for the plug-in to report temporary conditions that would cause the input trust authority (ITA) to distrust the plug-in. For example, if an EVR presenter is in windowed mode, it is vulnerable to GDI screen captures.

To disable screen capture in Direct3D, the plug-in must do the following:

<ul>
<li>
Create the Direct3D device in full-screen exlusive mode.

</li>
<li>
Specify the D3DCREATE_DISABLE_PRINTSCREEN flag when you create the device. For more information, see <b>IDirect3D9::CreateDevice</b> in the DirectX documentation.

</li>
</ul>
In addition, the graphics adapter must support the Windows Vista Display Driver Model (WDDM) and the Direct3D extensions for Windows Vista (sometimes called D3D9Ex or D3D9L).

If these conditions are met, the presenter can return <b>TRUE</b> in the <i>pYes</i> parameter. Otherwise, it should return <b>FALSE</b>.

The EVR calls this method whenever the device changes. If the plug-in returns <b>FALSE</b>, the EVR treats this condition as if the plug-in had a new output connector of unknown type. The policy object can then allow or block playback, depending on the ITA's policy.

This method should be used only to report transient conditions. A plug-in that is never in a trusted state should not implement the <a href="https://msdn.microsoft.com/1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe">IEVRTrustedVideoPlugin</a> interface at all.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe">IEVRTrustedVideoPlugin</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

