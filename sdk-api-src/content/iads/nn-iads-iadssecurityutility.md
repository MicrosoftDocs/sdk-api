---
UID: NN:iads.IADsSecurityUtility
title: IADsSecurityUtility (iads.h)
author: windows-sdk-content
description: The IADsSecurityUtility interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key.
old-location: adsi\iadssecurityutility.htm
tech.root: adsi
ms.assetid: 781eda1e-1f13-4bb4-ae8e-c9bf4c08e125
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsSecurityUtility, IADsSecurityUtility interface [ADSI], IADsSecurityUtility interface [ADSI],described, _ds_iadssecurityutility, adsi.iadssecurityutility, iads/IADsSecurityUtility
ms.topic: interface
f1_keywords: 
 - "iads/IADsSecurityUtility"
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsSecurityUtility interface


## -description


The <b>IADsSecurityUtility</b> interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key. You can also use it to convert the security descriptor to or from raw or hexadecimal mode and you can limit the scope of the security descriptor data retrieved or set by indicating whether you want it for the owner, group, DACL, or SACL.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityUtility</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsSecurityUtility</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsSecurityUtility</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadssecurityutility-convertsecuritydescriptor">ConvertSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Converts a security descriptor from one format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves a security descriptor for the specified file, fileshare, or registry key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor for the specified file, file share, or registry key.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityUtility</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadssecurityutility-get_securitymask">SecurityMask</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Determines which elements of the security descriptor to retrieve or set.

</td>
</tr>
</table> 


## -remarks



To read the system access-control list (SACL) of a file or directory, the <b>SE_SECURITY_NAME</b> privilege must be enabled for the calling process. For more information about retrieving the SACL for an object, see <a href="https://docs.microsoft.com/windows/desktop/AD/retrieving-an-objectampaposs-sacl">Retrieving an Object's SACL</a>.

For more information and a code example that shows how to use the <b>IADsSecurityUtility</b> interface to add an ACE to a file, see <a href="https://docs.microsoft.com/windows/desktop/ADSI/example-code-for-adding-an-ace-to-a-file">Example Code for Adding an ACE to a File</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="https://docs.microsoft.com/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/example-code-for-adding-an-ace-to-a-file">Example Code for Adding an ACE to a File</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IAccessControlList</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/security-descriptors-on-files-and-registry-keys">Security Descriptors on Files and Registry Keys</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/security-interfaces">Security Interfaces</a>
 

 

