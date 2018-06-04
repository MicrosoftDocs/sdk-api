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

# IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin


## -description



The <b>IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin</b> function removes information from the registry about a Windows Media Player plug-in.




## -parameters




### -param guidPluginType

GUID specifying plug-in type. For DSP plug-ins, specify WMP_PLUGINTYPE_DSP to register for DirectShow playback and WMP_PLUGINTYPE_DSP_OUTOFPROC for Media Foundation playback. See Remarks.


### -param clsid

Specifies the class ID of the plug-in being removed.


## -returns



The function returns an <b>HRESULT</b>.




## -remarks



Implement this function in the exported <b>DllUnRegisterServer</b> function.

DSP plug-ins designed to work with Windows Media Player 11 must call this method twice if <b>WMPRegisterPlayerPlugin</b> was called twice. The first call must specify <i>guidPluginType</i> as WMP_PLUGINTYPE_DSP. The second call must specify <i>guidPluginType</i> as WMP_PLUGINTYPE_DSP_OUTOFPROC. For plug-ins designed to be backward compatible, you should avoid making the second call when installing for earlier versions of Windows Media Player. To accomplish this, check the Windows version. If the Windows operating system major version is greater than or equal to 6, you can safely remove the plug-in for Media Foundation playback.




## -see-also




<a href="https://msdn.microsoft.com/4b99d227-39e8-4986-93ed-6df73a3a3e08">IWMPMediaPluginRegistrar Interface</a>



<a href="https://msdn.microsoft.com/db042911-c46f-431a-ad1c-ceb2c3b4546c">IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin</a>
 

 

