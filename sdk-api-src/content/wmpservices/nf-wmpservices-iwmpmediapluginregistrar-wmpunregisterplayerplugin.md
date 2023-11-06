---
UID: NF:wmpservices.IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin
title: IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin (wmpservices.h)
description: The IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin function removes information from the registry about a Windows Media Player plug-in.
helpviewer_keywords: ["IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin","IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin","WMPUnRegisterPlayerPlugin","WMPUnRegisterPlayerPlugin function [Windows Media Player]","wmp.iwmpmediapluginregistrar__wmpunregisterplayerplugin","wmpservices/WMPUnRegisterPlayerPlugin"]
old-location: wmp\iwmpmediapluginregistrar__wmpunregisterplayerplugin.htm
tech.root: WMP
ms.assetid: b6165962-3ca6-49c8-826c-ce87e55c09fd
ms.date: 4/26/2023
ms.keywords: IWMPMediaPluginRegistrar.WMPUnRegisterPlayerPlugin, IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin, WMPUnRegisterPlayerPlugin, WMPUnRegisterPlayerPlugin function [Windows Media Player], wmp.iwmpmediapluginregistrar__wmpunregisterplayerplugin, wmpservices/WMPUnRegisterPlayerPlugin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin
 - wmpservices/IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wmp.dll
api_name:
 - WMPUnRegisterPlayerPlugin
---

# IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar">IWMPMediaPluginRegistrar Interface</a>



<a href="/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin">IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin</a>