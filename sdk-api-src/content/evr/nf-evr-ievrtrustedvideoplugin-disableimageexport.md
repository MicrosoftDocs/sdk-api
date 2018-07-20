---
UID: NF:evr.IEVRTrustedVideoPlugin.DisableImageExport
title: IEVRTrustedVideoPlugin::DisableImageExport
author: windows-sdk-content
description: Enables or disables the ability of the plug-in to export the video image.
old-location: mf\ievrtrustedvideoplugin_disableimageexport.htm
old-project: medfound
ms.assetid: dd9811f7-7a9f-4b7e-8425-cb25efe0a71d
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DisableImageExport, DisableImageExport method [Media Foundation], DisableImageExport method [Media Foundation],IEVRTrustedVideoPlugin interface, IEVRTrustedVideoPlugin interface [Media Foundation],DisableImageExport method, IEVRTrustedVideoPlugin.DisableImageExport, IEVRTrustedVideoPlugin::DisableImageExport, dd9811f7-7a9f-4b7e-8425-cb25efe0a71d, evr/IEVRTrustedVideoPlugin::DisableImageExport, mf.ievrtrustedvideoplugin_disableimageexport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin.DisableImageExport
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRTrustedVideoPlugin::DisableImageExport


## -description



          Enables or disables the ability of the plug-in to export the video image.
        


## -parameters




### -param bDisable [in]

Boolean value. Specify <b>TRUE</b> to disable image exporting, or <b>FALSE</b> to enable it.


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



An EVR plug-in might expose a way for the application to get a copy of the video frames. For example, the standard EVR presenter implements <a href="https://msdn.microsoft.com/25ec4c23-04dd-4e18-9cc1-de9e57271e8f">IMFVideoDisplayControl::GetCurrentImage</a>.

If the plug-in supports image exporting, this method enables or disables it. Before this method has been called for the first time, the EVR assumes that the mechanism is enabled.

If the plug-in does not support image exporting, this method should return S_OK and ignore the value of <i>bDisable</i>. If the method fails, the EVR treats it as a failure to enforce the policy, which will probably cause playback to stop.

While image exporting is disabled, any associated export method, such as <a href="https://msdn.microsoft.com/25ec4c23-04dd-4e18-9cc1-de9e57271e8f">GetCurrentImage</a>, should return MF_E_LICENSE_INCORRECT_RIGHTS.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe">IEVRTrustedVideoPlugin</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

