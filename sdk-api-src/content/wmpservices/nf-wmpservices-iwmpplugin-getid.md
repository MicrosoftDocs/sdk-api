---
UID: NF:wmpservices.IWMPPlugin.GetID
title: IWMPPlugin::GetID (wmpservices.h)
description: The IWMPPlugin::GetID method returns the class id of the plug-in.
helpviewer_keywords: ["GetID","GetID method [Windows Media Player]","GetID method [Windows Media Player]","IWMPPlugin interface","IWMPPlugin interface [Windows Media Player]","GetID method","IWMPPlugin.GetID","IWMPPlugin::GetID","IWMPPluginGetIDDSP","wmp.iwmpplugin_getid","wmpservices/IWMPPlugin::GetID"]
old-location: wmp\iwmpplugin_getid.htm
tech.root: WMP
ms.assetid: 883b6e19-5d1a-4ad9-882b-953772e8e11a
ms.date: 12/05/2018
ms.keywords: GetID, GetID method [Windows Media Player], GetID method [Windows Media Player],IWMPPlugin interface, IWMPPlugin interface [Windows Media Player],GetID method, IWMPPlugin.GetID, IWMPPlugin::GetID, IWMPPluginGetIDDSP, wmp.iwmpplugin_getid, wmpservices/IWMPPlugin::GetID
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
 - IWMPPlugin::GetID
 - wmpservices/IWMPPlugin::GetID
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
 - IWMPPlugin.GetID
---

# IWMPPlugin::GetID


## -description

The <b>IWMPPlugin::GetID</b> method returns the class id of the plug-in.

## -parameters

### -param pGUID [out]

Pointer to a <b>GUID</b> that represents the class id of the plug-in.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

For more information on the <b>GUID</b> structure, see the Platform SDK.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin">IWMPPlugin Interface</a>