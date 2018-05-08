---
UID: NF:wmpservices.IWMPMediaPluginRegistrar.WMPRegisterPlayerPlugin
title: IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin
author: windows-driver-content
description: The IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin function adds information to the registry that identifies a Windows Media Player plug-in.
old-location: wmp\iwmpmediapluginregistrar__wmpregisterplayerplugin.htm
old-project: WMP
ms.assetid: db042911-c46f-431a-ad1c-ceb2c3b4546c
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IWMPMediaPluginRegistrar.WMPRegisterPlayerPlugin, IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin, WMPRegisterPlayerPlugin, WMPRegisterPlayerPlugin function [Windows Media Player], wmp.iwmpmediapluginregistrar__wmpregisterplayerplugin, wmpservices/WMPRegisterPlayerPlugin
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wmp.dll
api_name:
-	WMPRegisterPlayerPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin


## -description



The <b>IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin</b> function adds information to the registry that identifies a Windows Media Player plug-in.




## -parameters




### -param pwszFriendlyName

Pointer to a wide character null-terminated string containing the friendly name of the plug-in. This is also the name that displays to the user.


### -param pwszDescription

Pointer to a wide character null-terminated string containing the description of the plug-in. This information also displays to the user.


### -param pwszUninstallString

Pointer to a wide character null-terminated string containing the uninstall string.


### -param dwPriority

Integer value containing the priority position of the plug-in in the chain of currently enabled plug-ins.


### -param guidPluginType

GUID specifying plug-in type. For DSP plug-ins, specify WMP_PLUGINTYPE_DSP to register for DirectShow playback and WMP_PLUGINTYPE_DSP_OUTOFPROC for Media Foundation playback. See Remarks.


### -param clsid

The class ID of the plug-in.


### -param cMediaTypes

Count of media types supported by the plug-in.


### -param pMediaTypes

Pointer to an array of media types that enumerates the supported media types. Media types are stored as type/subtype pairs.


## -returns



The function returns an <b>HRESULT</b>.




## -remarks



Implement this function in the exported <b>DllRegisterServer</b> function.

The uninstall string is a command line string that Windows Media Player passes as the argument to the Windows <b>ShellExecute</b> function when the user chooses to remove the plug-in by clicking <b>Remove</b> in the Player plug-in configuration dialog box. This gives you a way to execute your own uninstall program that initiates from Windows Media Player.

Priority values start at zero. Most DSP plug-ins should specify a value between 1 and 10. Lower values place the plug-in closer to the rendering engine.

DSP plug-ins registered with identical values for <b>dwPriority</b> are ordered based on their position in the registry. Plug-ins located higher in the registry hierarchy are assigned a higher priority than plug-ins located lower in the registry hierarchy.

DSP plug-ins designed to work with Windows Media Player 11 must call this method twice. The first call must specify <i>guidPluginType</i> as WMP_PLUGINTYPE_DSP. The second call must specify <i>guidPluginType</i> as WMP_PLUGINTYPE_DSP_OUTOFPROC. For plug-ins designed to be backward compatible, you should avoid making the second call when installing for earlier versions of Windows Media Player. To accomplish this, check the Windows version. If the Windows operating system major version is greater than or equal to 6, you can safely register the plug-in for Media Foundation playback.




## -see-also




<a href="https://msdn.microsoft.com/4b99d227-39e8-4986-93ed-6df73a3a3e08">IWMPMediaPluginRegistrar Interface</a>



<a href="https://msdn.microsoft.com/b6165962-3ca6-49c8-826c-ce87e55c09fd">IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin</a>
 

 

