---
UID: NF:mfidl.IMFContentEnabler.AutomaticEnable
title: IMFContentEnabler::AutomaticEnable (mfidl.h)
description: Performs a content enabling action without any user interaction.
helpviewer_keywords: ["7be4c32f-d116-4a08-857f-1a59b5ccfb12","AutomaticEnable","AutomaticEnable method [Media Foundation]","AutomaticEnable method [Media Foundation]","IMFContentEnabler interface","IMFContentEnabler interface [Media Foundation]","AutomaticEnable method","IMFContentEnabler.AutomaticEnable","IMFContentEnabler::AutomaticEnable","mf.imfcontentenabler_automaticenable","mfidl/IMFContentEnabler::AutomaticEnable"]
old-location: mf\imfcontentenabler_automaticenable.htm
tech.root: mf
ms.assetid: 7be4c32f-d116-4a08-857f-1a59b5ccfb12
ms.date: 12/05/2018
ms.keywords: 7be4c32f-d116-4a08-857f-1a59b5ccfb12, AutomaticEnable, AutomaticEnable method [Media Foundation], AutomaticEnable method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],AutomaticEnable method, IMFContentEnabler.AutomaticEnable, IMFContentEnabler::AutomaticEnable, mf.imfcontentenabler_automaticenable, mfidl/IMFContentEnabler::AutomaticEnable
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentEnabler::AutomaticEnable
 - mfidl/IMFContentEnabler::AutomaticEnable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentEnabler.AutomaticEnable
---

# IMFContentEnabler::AutomaticEnable


## -description

Performs a content enabling action without any user interaction.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation is complete, the content enabler sends an <a href="/windows/desktop/medfound/meenablercompleted">MEEnablerCompleted</a> event. While the operation is in progress, the content enabler might send <a href="/windows/desktop/medfound/meenablerprogress">MEEnablerProgress</a> events.

To find out whether the content enabler supports this method, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported">IMFContentEnabler::IsAutomaticSupported</a>.

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>
