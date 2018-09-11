---
UID: NC:evr.MFCreateVideoMixerAndPresenter
title: MFCreateVideoMixerAndPresenter
author: windows-sdk-content
description: Creates the default video mixer and video presenter for the enhanced video renderer (EVR).
old-location: mf\mfcreatevideomixerandpresenter.htm
tech.root: medfound
ms.assetid: 1777027a-85bb-47d2-baf8-6f420282b01a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 1777027a-85bb-47d2-baf8-6f420282b01a, MFCreateVideoMixerAndPresenter, MFCreateVideoMixerAndPresenter callback, MFCreateVideoMixerAndPresenter callback function [Media Foundation], evr/MFCreateVideoMixerAndPresenter, mf.mfcreatevideomixerandpresenter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: evr.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoMixerAndPresenter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateVideoMixerAndPresenter callback function


## -description



Creates the default video mixer and video presenter for the enhanced video renderer (EVR).




## -parameters




### -param pMixerOwner [in]

Pointer to the owner of the video mixer. If the mixer is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.


### -param pPresenterOwner [in]

Pointer to the owner of the video presenter. If the presenter is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.


### -param riidMixer [in]

Interface identifier (IID) of the requested interface on the video mixer. The video mixer exposes the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface.


### -param ppvVideoMixer [out]

Receives a pointer to the requested interface on the video mixer. The caller must release the interface.


### -param riidPresenter [in]

IID of the requested interface on the video presenter. The video presenter exposes the <a href="https://msdn.microsoft.com/8f6e3132-03e9-4a2e-9160-e39d29cf2408">IMFVideoPresenter</a> interface.


### -param ppvVideoPresenter [out]

Receives a pointer to the requested interface on the video presenter. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
 




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

