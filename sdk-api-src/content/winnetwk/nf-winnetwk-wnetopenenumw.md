---
UID: NF:winnetwk.WNetOpenEnumW
title: WNetOpenEnumW function (winnetwk.h)
description: The WNetOpenEnum function starts an enumeration of network resources or existing connections. You can continue the enumeration by calling the WNetEnumResource function. (Unicode)
helpviewer_keywords: ["0", "RESOURCETYPE_ANY", "RESOURCETYPE_DISK", "RESOURCETYPE_PRINT", "RESOURCEUSAGE_ALL", "RESOURCEUSAGE_ATTACHED", "RESOURCEUSAGE_CONNECTABLE", "RESOURCEUSAGE_CONTAINER", "RESOURCE_CONNECTED", "RESOURCE_CONTEXT", "RESOURCE_GLOBALNET", "RESOURCE_REMEMBERED", "WNetOpenEnum", "WNetOpenEnum function [Windows Networking (WNet)]", "WNetOpenEnumW", "_win32_wnetopenenum", "winnetwk/WNetOpenEnum", "winnetwk/WNetOpenEnumW", "wnet.wnetopenenum"]
old-location: wnet\wnetopenenum.htm
tech.root: WNet
ms.assetid: d99a549a-bf27-497f-a3be-bbe2c668bf90
ms.date: 12/05/2018
ms.keywords: 0, RESOURCETYPE_ANY, RESOURCETYPE_DISK, RESOURCETYPE_PRINT, RESOURCEUSAGE_ALL, RESOURCEUSAGE_ATTACHED, RESOURCEUSAGE_CONNECTABLE, RESOURCEUSAGE_CONTAINER, RESOURCE_CONNECTED, RESOURCE_CONTEXT, RESOURCE_GLOBALNET, RESOURCE_REMEMBERED, WNetOpenEnum, WNetOpenEnum function [Windows Networking (WNet)], WNetOpenEnumA, WNetOpenEnumW, _win32_wnetopenenum, winnetwk/WNetOpenEnum, winnetwk/WNetOpenEnumA, winnetwk/WNetOpenEnumW, wnet.wnetopenenum
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetOpenEnumW (Unicode) and WNetOpenEnumA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetOpenEnumW
 - winnetwk/WNetOpenEnumW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetOpenEnum
 - WNetOpenEnumA
 - WNetOpenEnumW
---

# WNetOpenEnumW function


## -description

The
				<b>WNetOpenEnum</b> function starts an enumeration of network resources or existing connections. You can continue the enumeration by calling the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function.

## -parameters

### -param dwScope [in]

Scope of the enumeration. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_CONNECTED"></a><a id="resource_connected"></a><dl>
<dt><b>RESOURCE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all currently connected resources. The function ignores the <i>dwUsage</i> parameter. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_CONTEXT"></a><a id="resource_context"></a><dl>
<dt><b>RESOURCE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Enumerate only resources in the network context of the caller. Specify this value for a Network Neighborhood view. The function ignores the <i>dwUsage</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_GLOBALNET"></a><a id="resource_globalnet"></a><dl>
<dt><b>RESOURCE_GLOBALNET</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all resources on the network.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_REMEMBERED"></a><a id="resource_remembered"></a><dl>
<dt><b>RESOURCE_REMEMBERED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all remembered (persistent) connections. The function ignores the <i>dwUsage</i> parameter.

</td>
</tr>
</table>

### -param dwType [in]

Resource types to be enumerated. This parameter can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_ANY"></a><a id="resourcetype_any"></a><dl>
<dt><b>RESOURCETYPE_ANY</b></dt>
</dl>
</td>
<td width="60%">
All resources. This value cannot be combined with RESOURCETYPE_DISK or RESOURCETYPE_PRINT.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_DISK"></a><a id="resourcetype_disk"></a><dl>
<dt><b>RESOURCETYPE_DISK</b></dt>
</dl>
</td>
<td width="60%">
All disk resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_PRINT"></a><a id="resourcetype_print"></a><dl>
<dt><b>RESOURCETYPE_PRINT</b></dt>
</dl>
</td>
<td width="60%">
All print resources.

</td>
</tr>
</table>
 

If a network provider cannot distinguish between print and disk resources, it can enumerate all resources.

### -param dwUsage [in]

Resource usage type to be enumerated. This parameter can be a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
All resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONNECTABLE"></a><a id="resourceusage_connectable"></a><dl>
<dt><b>RESOURCEUSAGE_CONNECTABLE</b></dt>
</dl>
</td>
<td width="60%">
All connectable resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONTAINER"></a><a id="resourceusage_container"></a><dl>
<dt><b>RESOURCEUSAGE_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
All container resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_ATTACHED"></a><a id="resourceusage_attached"></a><dl>
<dt><b>RESOURCEUSAGE_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Setting this value forces 
<b>WNetOpenEnum</b> to fail if the user is not authenticated. The function fails even if the network allows enumeration without authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_ALL"></a><a id="resourceusage_all"></a><dl>
<dt><b>RESOURCEUSAGE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Setting this value is equivalent to setting RESOURCEUSAGE_CONNECTABLE, RESOURCEUSAGE_CONTAINER, and RESOURCEUSAGE_ATTACHED.

</td>
</tr>
</table>
 

This parameter is ignored unless the <i>dwScope</i> parameter is equal to RESOURCE_GLOBALNET. For more information, see the following Remarks section.

### -param lpNetResource [in]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcew">NETRESOURCE</a> structure that specifies the container to enumerate. If the <i>dwScope</i> parameter is not RESOURCE_GLOBALNET, this parameter must be <b>NULL</b>. 




If this parameter is <b>NULL</b>, the root of the network is assumed. (The system organizes a network as a hierarchy; the root is the topmost container in the network.)

If this parameter is not <b>NULL</b>, it must point to a 
<b>NETRESOURCE</b> structure. This structure can be filled in by the application or it can be returned by a call to the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function. The 
<b>NETRESOURCE</b> structure must specify a container resource; that is, the RESOURCEUSAGE_CONTAINER value must be specified in the <i>dwUsage</i> parameter.

To enumerate all network resources, an application can begin the enumeration by calling 
<b>WNetOpenEnum</b> with the <i>lpNetResource</i> parameter set to <b>NULL</b>, and then use the returned handle to call 
<b>WNetEnumResource</b> to enumerate resources. If one of the resources in the 
<b>NETRESOURCE</b> array returned by the 
<b>WNetEnumResource</b> function is a container resource, you can call 
<b>WNetOpenEnum</b> to open the resource for further enumeration.

### -param lphEnum [out]

Pointer to an enumeration handle that can be used in a subsequent call to 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpNetResource</i> parameter does not point to a container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>dwScope</i> or the <i>dwType</i> parameter is invalid, or there is an invalid combination of parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
A remote network resource name supplied in the <b>NETRESOURCE</b> structure resolved to an invalid network address.

</td>
</tr>
</table>

## -remarks

If the <i>dwScope</i> parameter is equal to RESOURCE_CONNECTED, a network connection made using the Microsoft LAN Manager network is omitted from the enumeration if the connection was made by an application running in a different logon session than the application calling the 
<b>WNetOpenEnum</b> function. This is because connections made using Microsoft LAN Manager are visible only to applications running in the same logon session as the application that made the connection. (To include the connection in the enumeration, it is not sufficient for the application to be running in the user account that created the connection.)

The exact interpretation of RESOURCE_CONTEXT in the <i>dwScope</i> parameter depends on the networks installed on the machine.

The 
<b>WNetOpenEnum</b> function is used to begin enumeration of the resources in a single container. The following examples show the hierarchical structure of a Microsoft LAN Manager network and a Novell NetWare network and identify the containers.


``` syntax
LanMan (container, in this case the provider) 
  ACCOUNTING (container, in this case the domain) 
    \\ACCTSPAY (container, in this case the server) 
      PAYFILES (disk) 
      LASERJET (print) 
 
NetWare (container, in this case the provider) 
  MARKETING (container, in this case the server) 
    SYS (disk, first one on any NetWare server) 
    ANOTHERVOLUME (disk) 
    LASERJET (print) 

```


#### Examples

For a code sample that illustrates an application-defined function that enumerates all the resources on a network, see 
<a href="/windows/desktop/WNet/enumerating-network-resources">Enumerating Network Resources</a>.

<div class="code"></div>




> [!NOTE]
> The winnetwk.h header defines WNetOpenEnum as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcew">NETRESOURCE</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcloseenum">WNetCloseEnum</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
