---
UID: NE:objidlbase.tagGLOBALOPT_PROPERTIES
title: GLOBALOPT_PROPERTIES (objidlbase.h)
description: Identifies process-global options that you can set or query by using the IGlobalOptions interface.helpviewer_keywords: ["COMGLB_APPID","COMGLB_EXCEPTION_HANDLING","COMGLB_RO_SETTINGS","COMGLB_RPC_THREADPOOL_SETTING","COMGLB_UNMARSHALING_POLICY","GLOBALOPT_PROPERTIES","GLOBALOPT_PROPERTIES enumeration [COM]","com.globalopt_properties","objidl/COMGLB_APPID","objidl/COMGLB_EXCEPTION_HANDLING","objidl/COMGLB_RO_SETTINGS","objidl/COMGLB_RPC_THREADPOOL_SETTING","objidl/COMGLB_UNMARSHALING_POLICY","objidl/GLOBALOPT_PROPERTIES"]
old-location: com\globalopt_properties.htm
tech.root: com
ms.assetid: 210BAEAF-D6FF-46E0-A187-D89EBB655B9C
ms.date: 12/05/2018
ms.keywords: COMGLB_APPID, COMGLB_EXCEPTION_HANDLING, COMGLB_RO_SETTINGS, COMGLB_RPC_THREADPOOL_SETTING, COMGLB_UNMARSHALING_POLICY, GLOBALOPT_PROPERTIES, GLOBALOPT_PROPERTIES enumeration [COM], com.globalopt_properties, objidl/COMGLB_APPID, objidl/COMGLB_EXCEPTION_HANDLING, objidl/COMGLB_RO_SETTINGS, objidl/COMGLB_RPC_THREADPOOL_SETTING, objidl/COMGLB_UNMARSHALING_POLICY, objidl/GLOBALOPT_PROPERTIES
f1_keywords:
- objidlbase/GLOBALOPT_PROPERTIES
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
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
- objidl.h
api_name:
- GLOBALOPT_PROPERTIES
targetos: Windows
req.typenames: GLOBALOPT_PROPERTIES
req.redist: 
ms.custom: 19H1
---

# GLOBALOPT_PROPERTIES enumeration


## -description


Identifies process-global options that you can set or query by using the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a> interface.


## -enum-fields




### -field COMGLB_EXCEPTION_HANDLING

Defines COM exception-handling behavior.


### -field COMGLB_APPID

Sets the AppID for the process.


### -field COMGLB_RPC_THREADPOOL_SETTING

Sets the thread-pool behavior of the RPC runtime in the process.


### -field COMGLB_RO_SETTINGS

Used for miscellaneous settings.


### -field COMGLB_UNMARSHALING_POLICY

Defines the policy that's applied in the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a> function.


### -field COMGLB_PROPERTIES_RESERVED1


### -field COMGLB_PROPERTIES_RESERVED2


### -field COMGLB_PROPERTIES_RESERVED3




## -remarks



The unmarshaling policy option <b>COMGLB_UNMARSHALING_POLICY</b> takes values from the <a href="https://docs.microsoft.com/windows/win32/api/objidl/ne-objidl-globalopt_unmarshaling_policy_values">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>



<a href="https://docs.microsoft.com/windows/win32/api/objidl/ne-objidl-globalopt_unmarshaling_policy_values">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>
 

 

