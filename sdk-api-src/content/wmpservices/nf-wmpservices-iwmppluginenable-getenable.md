---
UID: NF:wmpservices.IWMPPluginEnable.GetEnable
title: IWMPPluginEnable::GetEnable (wmpservices.h)
description: The IWMPPluginEnable::GetEnable method returns a value indicating whether Windows Media Player has enabled the plug-in.
helpviewer_keywords: ["GetEnable","GetEnable method [Windows Media Player]","GetEnable method [Windows Media Player]","IWMPPluginEnable interface","IWMPPluginEnable interface [Windows Media Player]","GetEnable method","IWMPPluginEnable.GetEnable","IWMPPluginEnable::GetEnable","IWMPPluginEnableGetEnableDSP","wmp.iwmppluginenable_getenable","wmpservices/IWMPPluginEnable::GetEnable"]
old-location: wmp\iwmppluginenable_getenable.htm
tech.root: WMP
ms.assetid: 29a08f6e-17a7-4bff-9aea-d5586d2b55b3
ms.date: 4/26/2023
ms.keywords: GetEnable, GetEnable method [Windows Media Player], GetEnable method [Windows Media Player],IWMPPluginEnable interface, IWMPPluginEnable interface [Windows Media Player],GetEnable method, IWMPPluginEnable.GetEnable, IWMPPluginEnable::GetEnable, IWMPPluginEnableGetEnableDSP, wmp.iwmppluginenable_getenable, wmpservices/IWMPPluginEnable::GetEnable
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPPluginEnable::GetEnable
 - wmpservices/IWMPPluginEnable::GetEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPPluginEnable.GetEnable
---

# IWMPPluginEnable::GetEnable


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPluginEnable::GetEnable</b> method returns a value indicating whether Windows Media Player has enabled the plug-in.

## -parameters

### -param pfEnable [out]

Pointer to a <b>Boolean</b> value indicating whether the user has enabled the plug-in.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

This value is set by Windows Media Player in the <b>IWMPPluginEnable::SetEnable</b> method.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable">IWMPPluginEnable Interface</a>



<a href="/windows/desktop/api/wmpservices/nf-wmpservices-iwmppluginenable-setenable">IWMPPluginEnable::SetEnable</a>