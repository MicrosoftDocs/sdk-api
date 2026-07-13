---
UID: NF:wmp.IWMPRemoteMediaServices.GetServiceType
title: IWMPRemoteMediaServices::GetServiceType (wmp.h)
description: The GetServiceType method is called by Windows Media Player to determine whether a host program wants to run its embedded control remotely.
helpviewer_keywords: ["GetServiceType","GetServiceType method [Windows Media Player]","GetServiceType method [Windows Media Player]","IWMPRemoteMediaServices interface","IWMPRemoteMediaServices interface [Windows Media Player]","GetServiceType method","IWMPRemoteMediaServices.GetServiceType","IWMPRemoteMediaServices::GetServiceType","IWMPRemoteMediaServicesGetServiceType","wmp.iwmpremotemediaservices_getservicetype","wmp/IWMPRemoteMediaServices::GetServiceType"]
old-location: wmp\iwmpremotemediaservices_getservicetype.htm
tech.root: WMP
ms.assetid: 866e7ee7-5df1-4e6b-8b41-85c6ff8b64d5
ms.date: 4/26/2023
ms.keywords: GetServiceType, GetServiceType method [Windows Media Player], GetServiceType method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetServiceType method, IWMPRemoteMediaServices.GetServiceType, IWMPRemoteMediaServices::GetServiceType, IWMPRemoteMediaServicesGetServiceType, wmp.iwmpremotemediaservices_getservicetype, wmp/IWMPRemoteMediaServices::GetServiceType
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later. Use of the RemoteNoDialogs value requires Windows Media Player 9 Series update 819756 or later. Use of the NoDialogs, NoDeviceSupport, or FindFolders values requires Windows Media Player 10.
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
 - IWMPRemoteMediaServices::GetServiceType
 - wmp/IWMPRemoteMediaServices::GetServiceType
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
 - IWMPRemoteMediaServices.GetServiceType
---

# IWMPRemoteMediaServices::GetServiceType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetServiceType</b> method is called by Windows Media Player to determine whether a host program wants to run its embedded control remotely.

## -parameters

### -param pbstrType [out]

Pointer to a <b></b>BSTR containing one or more of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Local</td>
<td>The Windows Media Player control is embedded in local mode.</td>
</tr>
<tr>
<td>NoDeviceSupport</td>
<td>The Windows Media Player control is embedded in remote mode and provides no support for device synchronization interfaces. Attempting to use device synchronization features in code when in this mode will result in the following error code: NS_E_PDA_DEVICESUPPORTDISABLED (0xC00D1190L). Requires Windows Media Player 10.</td>
</tr>
<tr>
<td>NoDialogs</td>
<td>Windows Media Player 10: The Windows Media Player control is embedded in remote mode and does not display dialog boxes. See Remarks.Windows Media Player 11: The Windows Media Player control is embedded in either local or remote mode and does not display dialog boxes.

</td>
</tr>
<tr>
<td>Remote</td>
<td>The Windows Media Player control is embedded in remote mode.</td>
</tr>
<tr>
<td>RemoteNoDialogs</td>
<td>The Windows Media Player control is embedded in remote mode and does not display dialog boxes. Use of this value requires Windows Media Player 9 Series update 819756 or later. See Remarks.</td>
</tr>
<tr>
<td>ExclusiveService:<i>keyname</i></td>
<td>The Windows Media Player control is embedded in remote mode, and service selector for online stores is disabled. The only online store available to the user is the one identified by <i>keyname</i>. If this value is combined with other values from this table, it must be the last value in the combination. Requires Windows Media Player 11.</td>
</tr>
</table>

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

You should avoid keeping a remoted instance of the Player running in the background during times when the control is not in use. Because the remoted Player control instance shares its playback engine with the full mode Player, keeping a background instance running can cause unexpected behavior. For example, the user might close the full mode Player while a file is playing. The user would expect that file playback would completely stop when the Player closes, but audio might continue to play because the playback engine is still active.

For Windows Media Player 10, the values for <i>pbstrType</i> may be used in combination by concatenating multiple values separated by spaces. For example, to use a remoted instance of Windows Media Player 10 that displays no dialog boxes and searches for digital media content, use "Remote NoDialogs FindFolders" as the value for <i>pbstrType</i>.

For Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store. In that case, the service selector is disabled and only the specified online store is available to the user. For more information, see Specifying an Exclusive Online Store in <a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.

NoDialogs, FindFolders, and Exclusive:<i>keyname</i> are valid only when combined with Remote. These values are not supported when combined with Local.

The RemoteNoDialogs value is supported for backward compatibility with Windows Media Player 9 Series. (See <a href="https://support.microsoft.com/?id=819756">Microsoft Knowledge Base Article - 819756</a> for more information.) For Windows Media Player 10, the recommended usage is "Remote NoDialogs".

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>