---
UID: NS:accctrl._ACTRL_ALISTW
title: ACTRL_ACCESSW (accctrl.h)
description: Contains an array of access-control lists for an object and its properties.helpviewer_keywords: ["*PACTRL_ACCESSW","*PACTRL_AUDITW","ACTRL_ACCESS","ACTRL_ACCESS structure [COM]","ACTRL_ACCESSA","ACTRL_ACCESSW","ACTRL_AUDIT","ACTRL_AUDITW","PACTRL_ACCESS","PACTRL_ACCESS structure pointer [COM]","PACTRL_ACCESSW_ALLOCATE_ALL_NODES","_ACTRL_ALISTA","_ACTRL_ALISTW","accctrl/ACTRL_ACCESS","accctrl/ACTRL_ACCESSA","accctrl/ACTRL_ACCESSW","accctrl/PACTRL_ACCESS","com.actrl_access"]
old-location: com\actrl_access.htm
tech.root: com
ms.assetid: d7fb10c1-ebb8-44cf-b61c-a70a787b324f
ms.date: 12/05/2018
ms.keywords: '*PACTRL_ACCESSW, *PACTRL_AUDITW, ACTRL_ACCESS, ACTRL_ACCESS structure [COM], ACTRL_ACCESSA, ACTRL_ACCESSW, ACTRL_AUDIT, ACTRL_AUDITW, PACTRL_ACCESS, PACTRL_ACCESS structure pointer [COM], PACTRL_ACCESSW_ALLOCATE_ALL_NODES, _ACTRL_ALISTA, _ACTRL_ALISTW, accctrl/ACTRL_ACCESS, accctrl/ACTRL_ACCESSA, accctrl/ACTRL_ACCESSW, accctrl/PACTRL_ACCESS, com.actrl_access'
f1_keywords:
- accctrl/ACTRL_ACCESS
dev_langs:
- c++
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_ACCESSW (Unicode) and ACTRL_ACCESSA (ANSI)
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
- HeaderDef
api_location:
- AccCtrl.h
api_name:
- ACTRL_ACCESS
- ACTRL_ACCESSA
- ACTRL_ACCESSW
targetos: Windows
req.typenames: ACTRL_ACCESSW, *PACTRL_ACCESSW, ACTRL_AUDITW, *PACTRL_AUDITW
req.redist: 
ms.custom: 19H1
---

# ACTRL_ACCESSW structure


## -description


Contains an array of access-control lists for an object and its properties.


## -struct-fields




### -field cEntries

The number of entries in the <b>pPropertyAccessList</b> array.


### -field pPropertyAccessList

An array of <a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-actrl_property_entrya">ACTRL_PROPERTY_ENTRY</a> structures. Each structure contains a list of access-control entries for an object or a specified property on the object.


### -field pPropertyAccessList.size_is

 


### -field pPropertyAccessList.size_is.cEntries

 




## -remarks



Note the following type definition.

<pre class="syntax" xml:space="preserve"><code>typedef PACTRL_ACCESSW PACTRL_ACCESSW_ALLOCATE_ALL_NODES;</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-grantaccessrights">IAccessControl::GrantAccessRights</a>
 

 

