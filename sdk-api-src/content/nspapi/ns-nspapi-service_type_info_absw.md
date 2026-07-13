---
UID: NS:nspapi._SERVICE_TYPE_INFO_ABSW
title: SERVICE_TYPE_INFO_ABSW (nspapi.h)
description: The SERVICE_TYPE_INFO_ABS structure contains information about a network service type. Use SERVICE_TYPE_INFO_ABS to add a network service type to a namespace. (Unicode)
helpviewer_keywords: ["*LPSERVICE_TYPE_INFO_ABSW","*PSERVICE_TYPE_INFO_ABSW","SERVICE_TYPE_INFO_ABS","SERVICE_TYPE_INFO_ABS structure [Winsock]","SERVICE_TYPE_INFO_ABSA","SERVICE_TYPE_INFO_ABSW","_win32_service_type_info_abs_2","nspapi/SERVICE_TYPE_INFO_ABS","nspapi/SERVICE_TYPE_INFO_ABSA","nspapi/SERVICE_TYPE_INFO_ABSW","winsock.service_type_info_abs_2"]
old-location: winsock\service_type_info_abs_2.htm
tech.root: WinSock
ms.assetid: 9adf92b0-1268-48c1-91e4-d05ad696ff06
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_TYPE_INFO_ABSW, *PSERVICE_TYPE_INFO_ABSW, SERVICE_TYPE_INFO_ABS, SERVICE_TYPE_INFO_ABS structure [Winsock], SERVICE_TYPE_INFO_ABSA, SERVICE_TYPE_INFO_ABSW, _win32_service_type_info_abs_2, nspapi/SERVICE_TYPE_INFO_ABS, nspapi/SERVICE_TYPE_INFO_ABSA, nspapi/SERVICE_TYPE_INFO_ABSW, winsock.service_type_info_abs_2'
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_TYPE_INFO_ABSW (Unicode) and SERVICE_TYPE_INFO_ABSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_TYPE_INFO_ABSW, *PSERVICE_TYPE_INFO_ABSW, *LPSERVICE_TYPE_INFO_ABSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_TYPE_INFO_ABSW
 - nspapi/_SERVICE_TYPE_INFO_ABSW
 - PSERVICE_TYPE_INFO_ABSW
 - nspapi/PSERVICE_TYPE_INFO_ABSW
 - SERVICE_TYPE_INFO_ABSW
 - nspapi/SERVICE_TYPE_INFO_ABSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - SERVICE_TYPE_INFO_ABS
 - SERVICE_TYPE_INFO_ABSA
 - SERVICE_TYPE_INFO_ABSW
---

# SERVICE_TYPE_INFO_ABSW structure


## -description

The 
<b>SERVICE_TYPE_INFO_ABS</b> structure contains information about a network service type. Use <b>SERVICE_TYPE_INFO_ABS</b> to add a network service type to a namespace.

## -struct-fields

### -field lpTypeName

Pointer to a zero-terminated string that is the name of the network service type. This name is the same in all namespaces, and is used by the 
<a href="/windows/desktop/api/nspapi/nf-nspapi-gettypebynamea">GetTypeByName</a> and 
<b>GetNameByType</b> functions.

### -field dwValueCount

Number of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a> structures in the <b>Values</b> member array that follows <b>dwValueCount</b>.

### -field Values

Array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a> structures. 




Each of these structures contains information about a service type value that the operating system or network service may need when an instance of this network service type is registered with a namespace.

The information in these structures may be specific to a namespace. For example, if a network service uses the SAP namespace, but does not have a <b>GUID</b> that contains the SAP identifier (SAPID), it defines the SAPID in a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a> structure.

## -remarks

When you use the 
<a href="/windows/desktop/api/nspapi/nf-nspapi-setservicea">SetService</a> function to add a network service type to a namespace, the 
<b>SERVICE_TYPE_INFO_ABS</b> structure is passed as the <b>ServiceSpecificInfo</b> BLOB member of a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structure. Although the <b>ServiceSpecificInfo</b> member generally should not contain pointers, an exception is made in the case of the 
<b>SERVICE_TYPE_INFO_ABS</b> and 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a> structures.





> [!NOTE]
> The nspapi.h header defines SERVICE_TYPE_INFO_ABS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a>



<a href="/windows/desktop/api/nspapi/nf-nspapi-setservicea">SetService</a>
