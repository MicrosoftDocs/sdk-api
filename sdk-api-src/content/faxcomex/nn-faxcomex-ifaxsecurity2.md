---
UID: NN:faxcomex.IFaxSecurity2
title: IFaxSecurity2 (faxcomex.h)

description: Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.
old-location: fax\_mfax_faxsecurity2_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\faxinto_z_ifaxsecurity2.htm

ms.date: 12/05/2018
ms.keywords: IFaxSecurity2, IFaxSecurity2 interface [Fax Service], IFaxSecurity2 interface [Fax Service],described, _mfax_faxsecurity2_cpp, fax._mfax_faxsecurity2_cpp, faxcomex/IFaxSecurity2
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxSecurity2"
dev_langs:
 - c++
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxSecurity2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxSecurity2 interface


## -description


Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSecurity2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxSecurity2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxSecurity2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-refresh-vb">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-save-vb">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity">FaxSecurity</a> object data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSecurity2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxsecurity2-get_descriptor">Descriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Represents the security descriptor for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-grantedrights-vb">GrantedRights</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a combination of the fax server access rights granted to the user referencing this property. For example, some users have permission to submit fax jobs with high priority while others have permission to submit jobs with normal or low priority only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-informationtype-vb">InformationType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves the security information type.

</td>
</tr>
</table> 


## -remarks



This interface is supported only on Windows Vista or later. For earlier versions of Windows use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a>.

Only an administrator with permissions can configure the security of the fax server. For more information, see <a href="https://docs.microsoft.com/windows/desktop/FWP/access-control">Access Control</a>.

A default implementation is provided as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a>. 



