---
UID: NN:mfidl.IMFTopologyNodeAttributeEditor
title: IMFTopologyNodeAttributeEditor (mfidl.h)
description: Updates the attributes of one or more nodes in the Media Session's current topology.
helpviewer_keywords: ["9ab384b9-0ce9-428c-a683-b09dbd4e07d9","IMFTopologyNodeAttributeEditor","IMFTopologyNodeAttributeEditor interface [Media Foundation]","IMFTopologyNodeAttributeEditor interface [Media Foundation]","described","mf.imftopologynodeattributeeditor","mfidl/IMFTopologyNodeAttributeEditor"]
old-location: mf\imftopologynodeattributeeditor.htm
tech.root: mf
ms.assetid: 9ab384b9-0ce9-428c-a683-b09dbd4e07d9
ms.date: 12/05/2018
ms.keywords: 9ab384b9-0ce9-428c-a683-b09dbd4e07d9, IMFTopologyNodeAttributeEditor, IMFTopologyNodeAttributeEditor interface [Media Foundation], IMFTopologyNodeAttributeEditor interface [Media Foundation],described, mf.imftopologynodeattributeeditor, mfidl/IMFTopologyNodeAttributeEditor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTopologyNodeAttributeEditor
 - mfidl/IMFTopologyNodeAttributeEditor
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
 - IMFTopologyNodeAttributeEditor
---

# IMFTopologyNodeAttributeEditor interface


## -description

Updates the attributes of one or more nodes in the Media Session's current topology.

The Media Session exposes this interface as a service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE.

## -inheritance

The <b>IMFTopologyNodeAttributeEditor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyNodeAttributeEditor</b> also has these types of members:

## -remarks

Currently the only attribute that can be updated is the <a href="/windows/desktop/medfound/mf-toponode-mediastop-attribute">MF_TOPONODE_MEDIASTOP</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
