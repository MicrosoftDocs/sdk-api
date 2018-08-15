---
UID: NE:wmcontainer.ASF_SELECTION_STATUS
title: ASF_SELECTION_STATUS
author: windows-sdk-content
description: Defines the selection options for an ASF stream.
old-location: mf\asf_selection_status.htm
old-project: medfound
ms.assetid: 1571650b-4d5c-49ae-9e6d-77ef4ae7ae59
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 1571650b-4d5c-49ae-9e6d-77ef4ae7ae59, ASF_SELECTION_STATUS, ASF_SELECTION_STATUS enumeration [Media Foundation], ASF_STATUS_ALLDATAUNITS, ASF_STATUS_CLEANPOINTSONLY, ASF_STATUS_NOTSELECTED, mf.asf_selection_status, wmcontainer/ASF_SELECTION_STATUS, wmcontainer/ASF_STATUS_ALLDATAUNITS, wmcontainer/ASF_STATUS_CLEANPOINTSONLY, wmcontainer/ASF_STATUS_NOTSELECTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmcontainer.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ASF_SELECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcontainer.h
api_name:
 - ASF_SELECTION_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ASF_SELECTION_STATUS enumeration


## -description



Defines the selection options for an ASF stream.




## -enum-fields




### -field ASF_STATUS_NOTSELECTED

No samples from the stream are delivered.


### -field ASF_STATUS_CLEANPOINTSONLY

Only samples from the stream that are clean points are delivered.


### -field ASF_STATUS_ALLDATAUNITS

All samples from the stream are delivered.


## -see-also




<a href="https://msdn.microsoft.com/82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c">IMFASFStreamSelector::GetBandwidthStep</a>



<a href="https://msdn.microsoft.com/64413669-bcb9-47fa-9362-b3f6831e55fb">IMFASFStreamSelector::GetOutputOverride</a>



<a href="https://msdn.microsoft.com/c8affecd-107f-4701-88df-200db06ad49e">IMFASFStreamSelector::SetOutputOverride</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

