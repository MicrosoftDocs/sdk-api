---
UID: NN:mfidl.IMFSensorTransformFactory
title: IMFSensorTransformFactory (mfidl.h)
description: The interface implemented by sensor transforms to allow the media pipeline to query requirements of the sensor transform and to create a runtime instance of the sensor transform.helpviewer_keywords: ["IMFSensorTransformFactory","IMFSensorTransformFactory interface [Media Foundation]","IMFSensorTransformFactory interface [Media Foundation]","described","mf.imfsensortransformfactory","mfidl/IMFSensorTransformFactory"]
old-location: mf\imfsensortransformfactory.htm
tech.root: medfound
ms.assetid: 291EA582-22E3-4646-8E89-74162E98203F
ms.date: 12/05/2018
ms.keywords: IMFSensorTransformFactory, IMFSensorTransformFactory interface [Media Foundation], IMFSensorTransformFactory interface [Media Foundation],described, mf.imfsensortransformfactory, mfidl/IMFSensorTransformFactory
f1_keywords:
- mfidl/IMFSensorTransformFactory
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.lib
- mfplat.dll
- mfplat.dll
- mfplat.dll.dll
api_name:
- IMFSensorTransformFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorTransformFactory interface


## -description


The interface implemented by sensor transforms to allow  the media pipeline to query requirements of the sensor transform and to create a runtime instance of the sensor transform.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorTransformFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorTransformFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorTransformFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensortransformfactory-createtransform">CreateTransform</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to create the transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensortransformfactory-gettransformcount">GetTransformCount</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get the number of transforms provided by the sensor transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensortransformfactory-gettransforminformation">GetTransformInformation</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to get information about a transform provided by the  sensor transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensortransformfactory-initializefactory">InitializeFactory</a>
</td>
<td align="left" width="63%">
Called by the media pipeline to initialize the sensor transform.

</td>
</tr>
</table> 

