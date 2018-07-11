---
UID: NE:vsmgmt._VSS_MGMT_OBJECT_TYPE
title: "_VSS_MGMT_OBJECT_TYPE"
author: windows-sdk-content
description: Discriminant for the VSS_MGMT_OBJECT_UNION union within the VSS_MGMT_OBJECT_PROP structure.
old-location: base\vss_mgmt_object_type.htm
old-project: vss
ms.assetid: ea28ff2c-6603-4193-9d5f-b41fffe28a90
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PVSS_MGMT_OBJECT_TYPE, PVSS_MGMT_OBJECT_TYPE, PVSS_MGMT_OBJECT_TYPE enumeration pointer [VSS], VSS_MGMT_OBJECT_DIFF_AREA, VSS_MGMT_OBJECT_DIFF_VOLUME, VSS_MGMT_OBJECT_TYPE, VSS_MGMT_OBJECT_TYPE enumeration [VSS], VSS_MGMT_OBJECT_UNKNOWN, VSS_MGMT_OBJECT_VOLUME, _VSS_MGMT_OBJECT_TYPE, base.vss_mgmt_object_type, vsmgmt/PVSS_MGMT_OBJECT_TYPE, vsmgmt/VSS_MGMT_OBJECT_DIFF_AREA, vsmgmt/VSS_MGMT_OBJECT_DIFF_VOLUME, vsmgmt/VSS_MGMT_OBJECT_TYPE, vsmgmt/VSS_MGMT_OBJECT_UNKNOWN, vsmgmt/VSS_MGMT_OBJECT_VOLUME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: VSS_MGMT_OBJECT_TYPE, *PVSS_MGMT_OBJECT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsMgmt.h
api_name:
 - VSS_MGMT_OBJECT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_MGMT_OBJECT_TYPE enumeration


## -description


The <b>VSS_MGMT_OBJECT_TYPE</b> enumeration type is a 
    discriminant for the <a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a> 
    union within the <a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> 
    structure.


## -enum-fields




### -field VSS_MGMT_OBJECT_UNKNOWN

The object type is unknown.


### -field VSS_MGMT_OBJECT_VOLUME

The object is a volume to be shadow copied.


### -field VSS_MGMT_OBJECT_DIFF_VOLUME

The object is a volume to hold a shadow copy storage area.


### -field VSS_MGMT_OBJECT_DIFF_AREA

The object is an association between a volume to be shadow copied and a volume to hold the shadow copy 
      storage area.


## -see-also




<a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a>



<a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a>
 

 

