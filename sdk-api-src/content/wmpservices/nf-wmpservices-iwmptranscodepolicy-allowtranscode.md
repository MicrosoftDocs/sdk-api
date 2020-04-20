---
UID: NF:wmpservices.IWMPTranscodePolicy.allowTranscode
title: IWMPTranscodePolicy::allowTranscode (wmpservices.h)
description: The allowTranscode method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.helpviewer_keywords: ["IWMPTranscodePolicy interface [Windows Media Player]","allowTranscode method","IWMPTranscodePolicy.allowTranscode","IWMPTranscodePolicy::allowTranscode","IWMPTranscodePolicyallowTranscode","allowTranscode","allowTranscode method [Windows Media Player]","allowTranscode method [Windows Media Player]","IWMPTranscodePolicy interface","wmp.iwmptranscodepolicy_allowtranscode","wmpservices/IWMPTranscodePolicy::allowTranscode"]
old-location: wmp\iwmptranscodepolicy_allowtranscode.htm
tech.root: WMP
ms.assetid: 6b43e247-cbb5-4ef1-8906-5ce7e1e58484
ms.date: 12/05/2018
ms.keywords: IWMPTranscodePolicy interface [Windows Media Player],allowTranscode method, IWMPTranscodePolicy.allowTranscode, IWMPTranscodePolicy::allowTranscode, IWMPTranscodePolicyallowTranscode, allowTranscode, allowTranscode method [Windows Media Player], allowTranscode method [Windows Media Player],IWMPTranscodePolicy interface, wmp.iwmptranscodepolicy_allowtranscode, wmpservices/IWMPTranscodePolicy::allowTranscode
f1_keywords:
- wmpservices/IWMPTranscodePolicy.allowTranscode
dev_langs:
- c++
req.header: wmpservices.h
req.include-header: 
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPTranscodePolicy.allowTranscode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPTranscodePolicy::allowTranscode


## -description



The <b>allowTranscode</b> method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.




## -parameters




### -param pvbAllow [out]

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

If the format used by a digital media file is not supported, Windows Media Player first checks the registry for existing permission to transcode, as described in <a href="https://docs.microsoft.com/windows/desktop/WMP/file-name-extension-registry-settings">File Name Extension Registry Settings</a>. If the custom format type is registered for permission to transcode, Windows Media Player locates the DirectShow source filter for the custom format type and calls <b>QueryInterface</b> to retrieve a pointer to <b>IWMPTranscodePolicy</b>. If the interface pointer is retrieved, the Player calls <b>IWMPTranscodePolicy::allowTranscode</b>. If <b>allowTranscode</b> returns VARIANT_TRUE, Windows Media Player performs the necessary transcoding. Otherwise, Windows Media Player does not copy the digital media file to the device. If any filter in the DirectShow graph returns VARIANT_FALSE from <b>allowTranscode</b>, the transcoding operation will fail.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy">IWMPTranscodePolicy Interface</a>
 

 

