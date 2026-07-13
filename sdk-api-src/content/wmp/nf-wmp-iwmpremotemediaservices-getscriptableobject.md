---
UID: NF:wmp.IWMPRemoteMediaServices.GetScriptableObject
title: IWMPRemoteMediaServices::GetScriptableObject (wmp.h)
description: The GetScriptableObject method is called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.
helpviewer_keywords: ["GetScriptableObject","GetScriptableObject method [Windows Media Player]","GetScriptableObject method [Windows Media Player]","IWMPRemoteMediaServices interface","IWMPRemoteMediaServices interface [Windows Media Player]","GetScriptableObject method","IWMPRemoteMediaServices.GetScriptableObject","IWMPRemoteMediaServices::GetScriptableObject","IWMPRemoteMediaServicesGetScriptableObject","wmp.iwmpremotemediaservices_getscriptableobject","wmp/IWMPRemoteMediaServices::GetScriptableObject"]
old-location: wmp\iwmpremotemediaservices_getscriptableobject.htm
tech.root: WMP
ms.assetid: c2e313fd-cbf6-4b0f-8eb0-1097af53e77a
ms.date: 4/26/2023
ms.keywords: GetScriptableObject, GetScriptableObject method [Windows Media Player], GetScriptableObject method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetScriptableObject method, IWMPRemoteMediaServices.GetScriptableObject, IWMPRemoteMediaServices::GetScriptableObject, IWMPRemoteMediaServicesGetScriptableObject, wmp.iwmpremotemediaservices_getscriptableobject, wmp/IWMPRemoteMediaServices::GetScriptableObject
req.header: wmp.h
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
 - IWMPRemoteMediaServices::GetScriptableObject
 - wmp/IWMPRemoteMediaServices::GetScriptableObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPRemoteMediaServices.GetScriptableObject
---

# IWMPRemoteMediaServices::GetScriptableObject


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetScriptableObject</b> method is called by Windows Media Player to retrieve a name and interface pointer for an object that can be called from the script code within a skin.

## -parameters

### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name of the scriptable object.

### -param ppDispatch [out]

Pointer to a pointer to the <b>IDispatch</b> interface of the scriptable object.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

The user interface of an embedded control can be customized by using Windows Media Player skin technology. You must specify a skin file location by using the <b>IWMPRemoteMediaServices::GetCustomUIMode</b> method. Skins used in this way can communicate with the host of the control through a scriptable object retrieved automatically by Windows Media Player through the <b>IWMPRemoteMediaServices::GetScriptableObject</b> method.

The embedded Windows Media Player control does not have to be remoted to use this method.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode">IWMPRemoteMediaServices::GetCustomUIMode</a>



<a href="/windows/desktop/WMP/using-skins-with-the-windows-media-player-control">Using Skins with the Windows Media Player Control</a>