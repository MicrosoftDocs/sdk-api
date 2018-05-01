---
UID: NF:vsmgmt.IVssEnumMgmtObject.Skip
title: IVssEnumMgmtObject::Skip method
author: windows-driver-content
description: Skips the specified number of objects.
old-location: base\ivssenummgmtobject_skip.htm
old-project: VSS
ms.assetid: ec53ac62-deb3-46f3-947a-1f6a4add4db2
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssEnumMgmtObject, IVssEnumMgmtObject interface [VSS], Skip method, IVssEnumMgmtObject::Skip, Skip method [VSS], Skip method [VSS], IVssEnumMgmtObject interface, Skip,IVssEnumMgmtObject.Skip, base.ivssenummgmtobject_skip, vsmgmt/IVssEnumMgmtObject::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VSS_PROTECTION_LEVEL, *PVSS_PROTECTION_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsMgmt.h
api_name:
-	IVssEnumMgmtObject.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssEnumMgmtObject::Skip method


## -description


The <b>Skip</b> method skips the specified 
    number of objects.


## -parameters




### -param celt [in]

Number of elements to be skipped in the list of enumerated objects.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c2067822-1824-4676-8376-7d83fcbbaea3">IVssEnumMgmtObject</a>
 

 

