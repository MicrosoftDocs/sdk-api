---
UID: NF:comsvcs.IComTrackingInfoProperties.GetPropName
title: IComTrackingInfoProperties::GetPropName (comsvcs.h)
author: windows-sdk-content
description: Retrieves the name of the property corresponding to the specified index number.
old-location: cos\icomtrackinginfoproperties_getpropname.htm
tech.root: cossdk
ms.assetid: 9a26bd3d-89e2-46fd-b9d1-b65ed12ae2ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPropName, GetPropName method [COM+], GetPropName method [COM+],IComTrackingInfoProperties interface, IComTrackingInfoProperties interface [COM+],GetPropName method, IComTrackingInfoProperties.GetPropName, IComTrackingInfoProperties::GetPropName, _dtc_IComTrackingInfoProperties_GetPropName, comsvcs/IComTrackingInfoProperties::GetPropName, cos.icomtrackinginfoproperties_getpropname
ms.topic: method
f1_keywords: ["comsvcs/IComTrackingInfoProperties.GetPropName"]
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTrackingInfoProperties.GetPropName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTrackingInfoProperties::GetPropName


## -description


Retrieves the name of the property corresponding to the specified index number.


## -parameters




### -param ulIndex [in]

The index of the property.


### -param ppszPropName [out]

The name of the property.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfoproperties">IComTrackingInfoProperties</a>
 

 

