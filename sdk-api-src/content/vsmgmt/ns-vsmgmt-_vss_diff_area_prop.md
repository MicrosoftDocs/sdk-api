---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _VSS_DIFF_AREA_PROP structure


## -description


The <b>VSS_DIFF_AREA_PROP</b> structure 
    describes associations between volumes containing the original file data and volumes containing the 
    shadow copy storage area (also known as the diff area).


## -struct-fields




### -field m_pwszVolumeName

The original volume name.


### -field m_pwszDiffAreaVolumeName

The shadow copy storage area volume name.


### -field m_llMaximumDiffSpace

Maximum space used on the shadow copy storage area volume for this association.


### -field m_llAllocatedDiffSpace

Allocated space on the shadow copy storage area volume by this association. This must be less than or equal 
      to <i>m_llMaximumDiffSpace</i>.


### -field m_llUsedDiffSpace

Used space from the allocated area above. This must be less than or equal 
      to <i>m_llAllocatedDiffSpace</i>.


## -remarks



The <b>m_llMaximumDiffSpace</b> member is passed as a parameter to the <a href="https://msdn.microsoft.com/7b58331c-b8a2-4333-a05d-563395d5f0c2">IVssDifferentialSoftwareSnapshotMgmt::AddDiffArea</a>, <a href="https://msdn.microsoft.com/c7773fa8-6b43-46bf-b644-0016b261c080">IVssDifferentialSoftwareSnapshotMgmt::ChangeDiffAreaMaximumSize</a>, and <a href="https://msdn.microsoft.com/9ba621d5-32ec-4512-a18f-dbdadbd3ff09">IVssDifferentialSoftwareSnapshotMgmt2::ChangeDiffAreaMaximumSizeEx</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/20cf12e4-4611-4e39-9f6f-e29f15e58b36">Volume Shadow Copy API Structures</a>
 

 

