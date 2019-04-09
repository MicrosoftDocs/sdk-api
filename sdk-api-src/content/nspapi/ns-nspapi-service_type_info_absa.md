---
UID: NS:nspapi._SERVICE_TYPE_INFO_ABSA
title: SERVICE_TYPE_INFO_ABSA (nspapi.h)
author: windows-sdk-content
description: The SERVICE_TYPE_INFO_ABS structure contains information about a network service type. Use SERVICE_TYPE_INFO_ABS to add a network service type to a namespace.
old-location: winsock\service_type_info_abs_2.htm
tech.root: WinSock
ms.assetid: 9adf92b0-1268-48c1-91e4-d05ad696ff06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSERVICE_TYPE_INFO_ABSA, *PSERVICE_TYPE_INFO_ABSA, SERVICE_TYPE_INFO_ABS, SERVICE_TYPE_INFO_ABS structure [Winsock], SERVICE_TYPE_INFO_ABSA, SERVICE_TYPE_INFO_ABSW, _win32_service_type_info_abs_2, nspapi/SERVICE_TYPE_INFO_ABS, nspapi/SERVICE_TYPE_INFO_ABSA, nspapi/SERVICE_TYPE_INFO_ABSW, winsock.service_type_info_abs_2"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SERVICE_TYPE_INFO_ABSA, *PSERVICE_TYPE_INFO_ABSA, *LPSERVICE_TYPE_INFO_ABSA
req.redist: 
---

# SERVICE_TYPE_INFO_ABSA structure


## -description


The 
<b>SERVICE_TYPE_INFO_ABS</b> structure contains information about a network service type. Use <b>SERVICE_TYPE_INFO_ABS</b> to add a network service type to a namespace.


## -struct-fields




### -field lpTypeName

Pointer to a zero-terminated string that is the name of the network service type. This name is the same in all namespaces, and is used by the 
<a href="https://msdn.microsoft.com/177bbae5-bc00-4ce5-a0f7-8474f0c2cb2e">GetTypeByName</a> and 
<b>GetNameByType</b> functions.


### -field dwValueCount

Number of 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures in the <b>Values</b> member array that follows <b>dwValueCount</b>.


### -field Values

Array of 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures. 




Each of these structures contains information about a service type value that the operating system or network service may need when an instance of this network service type is registered with a namespace.

The information in these structures may be specific to a namespace. For example, if a network service uses the SAP namespace, but does not have a <b>GUID</b> that contains the SAP identifier (SAPID), it defines the SAPID in a 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structure.


## -remarks



When you use the 
<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a> function to add a network service type to a namespace, the 
<b>SERVICE_TYPE_INFO_ABS</b> structure is passed as the <b>ServiceSpecificInfo</b> BLOB member of a 
<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a> structure. Although the <b>ServiceSpecificInfo</b> member generally should not contain pointers, an exception is made in the case of the 
<b>SERVICE_TYPE_INFO_ABS</b> and 
<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/6e3df308-3f5c-40d7-b0f9-19fb6d6d3db8">SERVICE_TYPE_VALUE_ABS</a>



<a href="https://msdn.microsoft.com/cc5e35ef-5c64-41ba-a5f9-5961371c4d08">SetService</a>
 

 

