---
UID: NN:sbe.IStreamBufferConfigure
title: IStreamBufferConfigure (sbe.h)
description: The IStreamBufferConfigure interface configures the location, number, and size of the backing files used by the various stream buffer objects.The StreamBufferConfig object exposes this interface.Before calling any of the Set methods on this interface, you must specify a registry key to hold the new settings. For more information, see IStreamBufferInitialize::SetHKEY.
helpviewer_keywords: ["IStreamBufferConfigure","IStreamBufferConfigure interface [Microsoft TV Technologies]","IStreamBufferConfigure interface [Microsoft TV Technologies]","described","IStreamBufferConfigureInterface","mstv.istreambufferconfigure","sbe/IStreamBufferConfigure"]
old-location: mstv\istreambufferconfigure.htm
tech.root: mstv
ms.assetid: 8874fefd-2241-4b04-a7d5-191e13743fa0
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure, IStreamBufferConfigure interface [Microsoft TV Technologies], IStreamBufferConfigure interface [Microsoft TV Technologies],described, IStreamBufferConfigureInterface, mstv.istreambufferconfigure, sbe/IStreamBufferConfigure
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IStreamBufferConfigure
 - sbe/IStreamBufferConfigure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure
---

# IStreamBufferConfigure interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferConfigure</b> interface configures the location, number, and size of the backing files used by the various stream buffer objects.

The <a href="/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object exposes this interface.

Before calling any of the <b>Set</b> methods on this interface, you must specify a registry key to hold the new settings. For more information, see <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">IStreamBufferInitialize::SetHKEY</a>.

## -inheritance

The <b>IStreamBufferConfigure</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferConfigure</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
