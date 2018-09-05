---
UID: NF:vsmgmt.IVssEnumMgmtObject.Next
title: IVssEnumMgmtObject::Next
author: windows-sdk-content
description: Returns the specified number of objects from the specified list of enumerated objects.
old-location: base\ivssenummgmtobject_next.htm
old-project: VSS
ms.assetid: 0ddcf25d-dc3e-4522-a98e-98d867230d42
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssEnumMgmtObject interface [VSS],Next method, IVssEnumMgmtObject.Next, IVssEnumMgmtObject::Next, Next, Next method [VSS], Next method [VSS],IVssEnumMgmtObject interface, base.ivssenummgmtobject_next, vsmgmt/IVssEnumMgmtObject::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsmgmt.h
req.include-header: 
req.redist: 
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
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssEnumMgmtObject.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssEnumMgmtObject::Next


## -description


The <b>Next</b> method 
    returns the specified number of objects from the specified list of enumerated objects.


## -parameters




### -param celt [in]

The number of elements to be read from the list of enumerated objects into the <i>rgelt</i> buffer.


### -param rgelt [out]

The address of a caller-allocated buffer that receives <i>celt</i><a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a> structures that contain the 
      returned objects. This parameter is required and cannot be <b>NULL</b>.


### -param pceltFetched [out]

The number of elements that were returned in the <i>rgelt</i> buffer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c2067822-1824-4676-8376-7d83fcbbaea3">IVssEnumMgmtObject</a>



<a href="https://msdn.microsoft.com/86681207-969e-4b33-aff8-79454ab04829">VSS_MGMT_OBJECT_PROP</a>
 

 

