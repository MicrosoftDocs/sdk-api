---
UID: NF:winnetwk.WNetGetResourceParentW
title: WNetGetResourceParentW function (winnetwk.h)
description: The WNetGetResourceParent function returns the parent of a network resource in the network browse hierarchy. Browsing begins at the location of the specified network resource. (Unicode)
helpviewer_keywords: ["WNetGetResourceParent", "WNetGetResourceParent function [Windows Networking (WNet)]", "WNetGetResourceParentW", "_win32_wnetgetresourceparent", "dwType", "lpProvider", "lpRemoteName", "winnetwk/WNetGetResourceParent", "winnetwk/WNetGetResourceParentW", "wnet.wnetgetresourceparent"]
old-location: wnet\wnetgetresourceparent.htm
tech.root: WNet
ms.assetid: 6ad5e2c0-d557-43cc-8ccf-a21160e262f8
ms.date: 12/05/2018
ms.keywords: WNetGetResourceParent, WNetGetResourceParent function [Windows Networking (WNet)], WNetGetResourceParentA, WNetGetResourceParentW, _win32_wnetgetresourceparent, dwType, lpProvider, lpRemoteName, winnetwk/WNetGetResourceParent, winnetwk/WNetGetResourceParentA, winnetwk/WNetGetResourceParentW, wnet.wnetgetresourceparent
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetResourceParentW (Unicode) and WNetGetResourceParentA (ANSI)
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
 - WNetGetResourceParentW
 - winnetwk/WNetGetResourceParentW
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
 - WNetGetResourceParent
 - WNetGetResourceParentA
 - WNetGetResourceParentW
---

# WNetGetResourceParentW function


## -description

The
				<b>WNetGetResourceParent</b> function returns the parent of a network resource in the network browse hierarchy. Browsing begins at the location of the specified network resource.

Call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa">WNetGetResourceInformation</a> and 
<b>WNetGetResourceParent</b> functions to move up the network hierarchy. Call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a> function to move down the hierarchy.

## -parameters

### -param lpNetResource [in]

Pointer to a <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure that specifies the network resource for which the parent name is required. 




Specify the members of the input 
<b>NETRESOURCE</b> structure as follows. The caller typically knows the values to provide for the <b>lpProvider</b> and <b>dwType</b> members after previous calls to 
<b>WNetGetResourceInformation</b> or 
<b>WNetGetResourceParent</b>.

<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dwType"></a><a id="dwtype"></a><a id="DWTYPE"></a><dl>
<dt><b>dwType</b></dt>
</dl>
</td>
<td width="60%">
This member should be filled in if known; otherwise, it should be set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="lpRemoteName"></a><a id="lpremotename"></a><a id="LPREMOTENAME"></a><dl>
<dt><b>lpRemoteName</b></dt>
</dl>
</td>
<td width="60%">
This member should specify the remote name of the network resource whose parent is required.

</td>
</tr>
<tr>
<td width="40%"><a id="lpProvider"></a><a id="lpprovider"></a><a id="LPPROVIDER"></a><dl>
<dt><b>lpProvider</b></dt>
</dl>
</td>
<td width="60%">
This member should specify the network provider that owns the resource. This member is required; otherwise, the function could produce incorrect results.

</td>
</tr>
</table>
 

All other members of the 
<b>NETRESOURCE</b> structure are ignored.

### -param lpBuffer [out]

Pointer to a buffer to receive a single 
<b>NETRESOURCE</b> structure that represents the parent resource. The function returns the <b>lpRemoteName</b>, <b>lpProvider</b>, <b>dwType</b>, <b>dwDisplayType</b>, and <b>dwUsage</b> members of the structure; all other members are set to <b>NULL</b>. 




The <b>lpRemoteName</b> member points to the remote name for the parent resource. This name uses the same syntax as the one returned from an enumeration by the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function. The caller can perform a string comparison to determine whether the 
<b>WNetGetResourceParent</b> resource is the same as that returned by 
<b>WNetEnumResource</b>. If the input resource has no parent on any of the networks, the <b>lpRemoteName</b> member is returned as <b>NULL</b>.

The presence of the RESOURCEUSAGE_CONNECTABLE bit in the <b>dwUsage</b> member indicates that you can connect to the parent resource, but only when it is available on the network.

### -param lpcbBuffer [in, out]

Pointer to a location that, on entry, specifies the size of the <i>lpBuffer</i> buffer, in bytes. If the buffer is too small to hold the result, this location receives the required buffer size, and the function returns ERROR_MORE_DATA.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The input <b>lpRemoteName</b> member is not an existing network resource for any network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The input <b>lpProvider</b> member does not match any installed network provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpBuffer</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_AUTHENTICATED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the necessary permissions to obtain the name of the parent.

</td>
</tr>
</table>

## -remarks

The 
<b>WNetGetResourceParent</b> function is typically used in conjunction with the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa">WNetGetResourceInformation</a> function to parse and interpret a network path typed in by a user.

Unlike the 
<b>WNetGetResourceInformation</b> function, if the resource includes a parent in its syntax, the 
<b>WNetGetResourceParent</b> function returns the parent, whether or not the resource actually exists. 
<b>WNetGetResourceParent</b> should typically be used only by applications that display network resources to the user in a hierarchical fashion. The Windows Explorer and the <b>File Open</b> dialog box are two well-known examples of this type of application. Note that no assumptions should be made about the type of resource that will be returned.

You can call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a>, 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa">WNetGetResourceInformation</a>, or 
<b>WNetGetResourceParent</b> function to return information from the 
<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure. You can also construct network resource information using the members of the 
<b>NETRESOURCE</b> structure.

An example of an inappropriate use of 
<b>WNetGetResourceParent</b> is to determine the name of the domain to which a specified server belongs. The function may happen to return the correct domain name for some networks in which domains appear directly above servers in the browse hierarchy. The function will return incorrect results for other networks.





> [!NOTE]
> The winnetwk.h header defines WNetGetResourceParent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa">WNetGetNetworkInformation</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetprovidernamea">WNetGetProviderName</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa">WNetGetResourceInformation</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea">WNetGetUniversalName</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
