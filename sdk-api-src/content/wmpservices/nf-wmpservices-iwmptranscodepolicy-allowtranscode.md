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
<th>
                  Value
                </th>
<th>
                  Description
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
 

 

