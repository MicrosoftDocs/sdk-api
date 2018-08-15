---
UID: NF:wmpservices.IWMPTranscodePolicy.allowTranscode
title: IWMPTranscodePolicy::allowTranscode
author: windows-sdk-content
description: The allowTranscode method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.
old-location: wmp\iwmptranscodepolicy_allowtranscode.htm
old-project: WMP
ms.assetid: 6b43e247-cbb5-4ef1-8906-5ce7e1e58484
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPTranscodePolicy interface [Windows Media Player],allowTranscode method, IWMPTranscodePolicy.allowTranscode, IWMPTranscodePolicy::allowTranscode, IWMPTranscodePolicyallowTranscode, allowTranscode, allowTranscode method [Windows Media Player], allowTranscode method [Windows Media Player],IWMPTranscodePolicy interface, wmp.iwmptranscodepolicy_allowtranscode, wmpservices/IWMPTranscodePolicy::allowTranscode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmpservices.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
tech.root: 
req.typenames: WMPServices_StreamState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPTranscodePolicy.allowTranscode
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPTranscodePolicy::allowTranscode


## -description



The <b>allowTranscode</b> method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.




## -parameters




### -param pvbAllow






#### - pvarfAllow [out]

Pointer to a <b>VARIANT_BOOL</b> that contains a value indicating whether transcoding is permitted.


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



When you copy to a device a digital media file that is in a custom format, you must change the format of the content if the device does not support the custom format. This process is called transcoding.

If the format used by a digital media file is not supported, Windows Media Player first checks the registry for existing permission to transcode, as described in <a href="https://msdn.microsoft.com/a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973">File Name Extension Registry Settings</a>. If the custom format type is registered for permission to transcode, Windows Media Player locates the DirectShow source filter for the custom format type and calls <b>QueryInterface</b> to retrieve a pointer to <b>IWMPTranscodePolicy</b>. If the interface pointer is retrieved, the Player calls <b>IWMPTranscodePolicy::allowTranscode</b>. If <b>allowTranscode</b> returns VARIANT_TRUE, Windows Media Player performs the necessary transcoding. Otherwise, Windows Media Player does not copy the digital media file to the device. If any filter in the DirectShow graph returns VARIANT_FALSE from <b>allowTranscode</b>, the transcoding operation will fail.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/b7dbd25f-6865-44fa-9d46-e77de393ce13">IWMPTranscodePolicy Interface</a>
 

 

