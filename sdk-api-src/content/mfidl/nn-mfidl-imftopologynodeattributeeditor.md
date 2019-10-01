---
UID: NN:mfidl.IMFTopologyNodeAttributeEditor
title: IMFTopologyNodeAttributeEditor (mfidl.h)
author: windows-sdk-content
description: Updates the attributes of one or more nodes in the Media Session's current topology.
old-location: mf\imftopologynodeattributeeditor.htm
tech.root: medfound
ms.assetid: 9ab384b9-0ce9-428c-a683-b09dbd4e07d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9ab384b9-0ce9-428c-a683-b09dbd4e07d9, IMFTopologyNodeAttributeEditor, IMFTopologyNodeAttributeEditor interface [Media Foundation], IMFTopologyNodeAttributeEditor interface [Media Foundation],described, mf.imftopologynodeattributeeditor, mfidl/IMFTopologyNodeAttributeEditor
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFTopologyNodeAttributeEditor"
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNodeAttributeEditor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopologyNodeAttributeEditor interface


## -description


Updates the attributes of one or more nodes in the Media Session's current topology.

The Media Session exposes this interface as a service. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyNodeAttributeEditor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyNodeAttributeEditor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopologyNodeAttributeEditor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes">UpdateNodeAttributes</a>
</td>
<td align="left" width="63%">
Updates the attributes of one or more nodes in the current topology.

</td>
</tr>
</table> 


## -remarks



Currently the only attribute that can be updated is the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-toponode-mediastop-attribute">MF_TOPONODE_MEDIASTOP</a> attribute.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

