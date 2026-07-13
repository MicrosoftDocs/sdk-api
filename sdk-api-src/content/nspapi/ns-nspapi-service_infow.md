---
UID: NS:nspapi._SERVICE_INFOW
title: SERVICE_INFOW (nspapi.h)
description: Contains information about a network service or a network service type. (Unicode)
helpviewer_keywords: ["*LPSERVICE_INFOW","*PSERVICE_INFOW","RESOURCEDISPLAYTYPE_DOMAIN","RESOURCEDISPLAYTYPE_FILE","RESOURCEDISPLAYTYPE_GENERIC","RESOURCEDISPLAYTYPE_GROUP","RESOURCEDISPLAYTYPE_SERVER","RESOURCEDISPLAYTYPE_SHARE","RESOURCEDISPLAYTYPE_TREE","SERVICE_INFO","SERVICE_INFO structure [Winsock]","SERVICE_INFOA","SERVICE_INFOW","_win32_service_info_2","nspapi/SERVICE_INFO","nspapi/SERVICE_INFOA","nspapi/SERVICE_INFOW","winsock.service_info_2"]
old-location: winsock\service_info_2.htm
tech.root: WinSock
ms.assetid: e76e0c1b-8cbf-45ad-a685-fb672801c24d
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_INFOW, *PSERVICE_INFOW, RESOURCEDISPLAYTYPE_DOMAIN, RESOURCEDISPLAYTYPE_FILE, RESOURCEDISPLAYTYPE_GENERIC, RESOURCEDISPLAYTYPE_GROUP, RESOURCEDISPLAYTYPE_SERVER, RESOURCEDISPLAYTYPE_SHARE, RESOURCEDISPLAYTYPE_TREE, SERVICE_INFO, SERVICE_INFO structure [Winsock], SERVICE_INFOA, SERVICE_INFOW, _win32_service_info_2, nspapi/SERVICE_INFO, nspapi/SERVICE_INFOA, nspapi/SERVICE_INFOW, winsock.service_info_2'
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_INFOW (Unicode) and SERVICE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_INFOW, *PSERVICE_INFOW, *LPSERVICE_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_INFOW
 - nspapi/_SERVICE_INFOW
 - PSERVICE_INFOW
 - nspapi/PSERVICE_INFOW
 - SERVICE_INFOW
 - nspapi/SERVICE_INFOW
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
 - SERVICE_INFO
 - SERVICE_INFOA
 - SERVICE_INFOW
---

# SERVICE_INFOW structure


## -description

The 
<b>SERVICE_INFO</b> structure contains information about a network service or a network service type.

## -struct-fields

### -field lpServiceType

Type: <b>LPGUID</b>

A pointer to a GUID that is the type of the network service.

### -field lpServiceName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated string that is the name of the network service. 




If you are calling the 
<b>SetService</b> function with the <i>dwNameSpace</i> parameter set to NS_DEFAULT, the network service name must be a common name. A common name is what the network service is commonly known as. An example of a common name for a network service is "My SQL Server".

If you are calling the 
<b>SetService</b> function with the <i>dwNameSpace</i> parameter set to a specific service name, the network service name can be a common name or a distinguished name. A distinguished name distinguishes the service to a unique location with a directory service. An example of a distinguished name for a network service is "MS\\SYS\\NT\\DEV\\My SQL Server".

### -field lpComment

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated string that is a comment or description for the network service. For example, "Used for development upgrades."

### -field lpLocale

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated string that contains locale information.

### -field dwDisplayHint

Type: <b>DWORD</b>

A hint as to how to display the network service in a network browsing user interface. This can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_DOMAIN"></a><a id="resourcedisplaytype_domain"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a domain.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_FILE"></a><a id="resourcedisplaytype_file"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_FILE</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a file.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_GENERIC"></a><a id="resourcedisplaytype_generic"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_GENERIC</b></dt>
</dl>
</td>
<td width="60%">
The method used to display the object does not matter.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_GROUP"></a><a id="resourcedisplaytype_group"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_GROUP</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a group.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SERVER"></a><a id="resourcedisplaytype_server"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a server.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SHARE"></a><a id="resourcedisplaytype_share"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SHARE</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a sharepoint.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_TREE"></a><a id="resourcedisplaytype_tree"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_TREE</b></dt>
</dl>
</td>
<td width="60%">
Display the network service as a tree.

</td>
</tr>
</table>

### -field dwVersion

Type: <b>DWORD</b>

The version for the network service. The high word of this value specifies a major version number. The low word of this value specifies a minor version number.

### -field dwTime

Type: <b>DWORD</b>

Reserved for future use. Must be zero.

### -field lpMachineName

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated string that is the name of the computer on which the network service is running.

### -field lpServiceAddress

Type: <b>LPSERVICE_ADDRESSES</b>

A pointer to a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_addresses">SERVICE_ADDRESSES</a> structure that contains an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a> structures. Each 
<b>SERVICE_ADDRESS</b> structure contains information about a network service address. 




A network service can call the 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function to determine the local address of the system.

### -field ServiceSpecificInfo

Type: <b>BLOB</b>

A 
						<a href="/windows/desktop/api/nspapi/ns-nspapi-blob">BLOB</a> structure that specifies service-defined information. 




<div class="alert"><b>Note</b>  In general, the data pointed to by the 
<a href="/windows/desktop/api/nspapi/ns-nspapi-blob">BLOB</a> structure's <b>pBlobData</b> member must not contain any pointers. That is because only the network service knows the format of the data; copying the data without such knowledge would lead to pointer invalidation. If the data pointed to by <b>pBlobData</b> contains variable-sized elements, offsets from <b>pBlobData</b> can be used to indicate the location of those elements. There is one exception to this general rule: when <b>pBlobData</b> points to a 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_info_absa">SERVICE_TYPE_INFO_ABS</a> structure. This is possible because both the 
<b>SERVICE_TYPE_INFO_ABS</b> structure, and any 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a> structures it contains are predefined, and thus their formats are known to the operating system.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-blob">BLOB</a>



<a href="/windows/desktop/api/nspapi/nf-nspapi-getservicea">GetService</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-ns_service_infoa">NS_SERVICE_INFO</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_addresses">SERVICE_ADDRESSES</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_info_absa">SERVICE_TYPE_INFO_ABS</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_type_value_absa">SERVICE_TYPE_VALUE_ABS</a>



<a href="/windows/desktop/api/nspapi/nf-nspapi-setservicea">SetService</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines SERVICE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
