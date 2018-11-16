---
UID: NF:wmpservices.IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin
title: IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin
author: windows-sdk-content
description: The IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin function removes information from the registry about a Windows Media Player plug-in.
old-location: wmp\iwmpmediapluginregistrar__wmpunregisterplayerplugin.htm
tech.root: WMP
ms.assetid: b6165962-3ca6-49c8-826c-ce87e55c09fd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin, IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin, WMPUnRegisterPlayerPlugin, WMPUnRegisterPlayerPlugin function [Windows Media Player], wmp.iwmpmediapluginregistrar__wmpunregisterplayerplugin, wmpservices/WMPUnRegisterPlayerPlugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wmp.dll
api_name:
 - WMPUnRegisterPlayerPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmpservices.h
: 
- IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin
: 
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
 

 

