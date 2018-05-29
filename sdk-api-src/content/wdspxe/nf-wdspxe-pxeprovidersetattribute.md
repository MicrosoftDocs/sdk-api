---
UID: NF:wdspxe.PxeProviderSetAttribute
title: PxeProviderSetAttribute function
author: windows-sdk-content
description: Specifies attributes for the provider.
old-location: wds\pxeprovidersetattribute.htm
old-project: Wds
ms.assetid: 01f7b50b-966b-4ff9-b933-851eaf1f1411
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PXE_PROV_ATTR_FILTER, PXE_PROV_ATTR_FILTER_IPV6, PXE_PROV_ATTR_IPV6_CAPABLE, PXE_PROV_FILTER_ALL, PXE_PROV_FILTER_DHCP_ONLY, PXE_PROV_FILTER_PXE_ONLY, PxeProviderSetAttribute, PxeProviderSetAttribute function [Windows Deployment Services], wds.pxeprovidersetattribute, wdspxe/PxeProviderSetAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WdsPxe.dll
api_name:
-	PxeProviderSetAttribute
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeProviderSetAttribute function


## -description


Specifies attributes for the provider.


## -parameters




### -param hProvider [in]

<b>HANDLE</b> passed to 
      the <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> function.


### -param Attribute [in]

Identifies the attribute to set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_ATTR_FILTER"></a><a id="pxe_prov_attr_filter"></a><dl>
<dt><b>PXE_PROV_ATTR_FILTER</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <i>pParameterBuffer</i> parameter points to a <b>ULONG</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_ATTR_FILTER_IPV6"></a><a id="pxe_prov_attr_filter_ipv6"></a><dl>
<dt><b>PXE_PROV_ATTR_FILTER_IPV6</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <i>pParameterBuffer</i> parameter points to a <b>ULONG</b>. Use this attribute with DHCPv6 packets. Available beginning with Windows 8 and Windows Server 2012.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_ATTR_IPV6_CAPABLE"></a><a id="pxe_prov_attr_ipv6_capable"></a><dl>
<dt><b>PXE_PROV_ATTR_IPV6_CAPABLE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Pointer to a <b>BOOL</b> value that is TRUE to indicate the provider is capable of processing IPv6 packets.  By default, the server assumes a provider is not capable of processing IPv6 packets and will not deliver them. Available beginning with Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


### -param pParameterBuffer [in]

Pointer to a buffer. The size and contents of this buffer vary depending on the value of the 
      <i>Attribute</i> parameter.


If <i>Attribute</i> is PXE_PROV_ATTR_FILTER, the buffer contains one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_FILTER_ALL"></a><a id="pxe_prov_filter_all"></a><dl>
<dt><b>PXE_PROV_FILTER_ALL</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Provider is to see all packets.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_FILTER_DHCP_ONLY"></a><a id="pxe_prov_filter_dhcp_only"></a><dl>
<dt><b>PXE_PROV_FILTER_DHCP_ONLY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Provider will see only DHCP packets. If <b>PXE_PROV_ATTR_FILTER_IPV6</b>, the provider will see only only DHCPv6 packets

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_PROV_FILTER_PXE_ONLY"></a><a id="pxe_prov_filter_pxe_only"></a><dl>
<dt><b>PXE_PROV_FILTER_PXE_ONLY</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Provider will see only DHCP packets that specify the DHCP Vendor Class Identifier option (60) as 
         "PXEClient". If <b>PXE_PROV_ATTR_FILTER_IPV6</b>,  provider will see only packets that specify a DHCPv6 OPTION_VENDOR_CLASS containing the “PXEClient”. 

</td>
</tr>
</table>
 


### -param uParamLen [in]

The size of the buffer pointed to by the <i>pParameterBuffer</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

