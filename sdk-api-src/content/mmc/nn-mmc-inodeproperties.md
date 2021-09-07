---
UID: NN:mmc.INodeProperties
title: INodeProperties (mmc.h)
description: The INodeProperties interface retrieves text-only properties for a node.
helpviewer_keywords: ["INodeProperties","INodeProperties interface [MMC]","INodeProperties interface [MMC]","described","_slate_inodeproperties","mmc.inodeproperties","mmc/INodeProperties"]
old-location: mmc\inodeproperties.htm
tech.root: mmc
ms.assetid: 5ef78fb9-704e-4c1d-ada8-c257a0944c94
ms.date: 12/05/2018
ms.keywords: INodeProperties, INodeProperties interface [MMC], INodeProperties interface [MMC],described, _slate_inodeproperties, mmc.inodeproperties, mmc/INodeProperties
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - INodeProperties
 - mmc/INodeProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - INodeProperties
---

# INodeProperties interface


## -description

The 
<b>INodeProperties</b> interface retrieves text-only properties for a node. This interface is implemented by snap-ins and its methods are called by the 
<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension">Extended View</a> extension that ships with MMC 2.0. Other view extensions and the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a> (particularly the 
<a href="/previous-versions/windows/desktop/mmc/node-object">Node</a>) can also use the 
<b>INodeProperties</b> interface.

The 
<b>INodeProperties</b> interface is queried (using 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>) from the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface for scope nodes, and from the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface for result items.

The Extended View extension queries two properties, CCF_DESCRIPTION and CCF_HTML_DETAILS. Instead of implementing 
<b>INodeProperties</b>, a snap-in can return values for these properties through data-object clipboard formats. The 
<b>INodeProperties</b> interface is available to snap-in developers whose data objects may not readily provide the property values.

## -inheritance

The <b>INodeProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INodeProperties</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-description">CCF_DESCRIPTION clipboard format</a>



<a href="/previous-versions/windows/desktop/mmc/ccf-html-details">CCF_HTML_DETAILS clipboard format</a>



<a href="/previous-versions/windows/desktop/mmc/node-object">Node object</a>



<a href="/previous-versions/windows/desktop/mmc/node-property">Node.Property</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension">Using the Extended View Extension</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension-implementation-details">Using the Extended View Extension - Implementation Details</a>
