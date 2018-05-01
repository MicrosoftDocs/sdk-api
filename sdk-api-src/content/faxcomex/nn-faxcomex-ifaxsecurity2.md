---
UID: NN:faxcomex.IFaxSecurity2
title: IFaxSecurity2
author: windows-driver-content
description: Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.
old-location: fax\_mfax_faxsecurity2_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\faxinto_z_ifaxsecurity2.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxSecurity2, IFaxSecurity2 interface [Fax Service], IFaxSecurity2 interface [Fax Service], described, _mfax_faxsecurity2_cpp, fax._mfax_faxsecurity2_cpp, faxcomex/IFaxSecurity2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxSecurity2
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSecurity2 interface


## -description


Used by a fax client application to configure the security on a fax server; also permits the calling application to set and retrieve a security descriptor for the fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSecurity2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxSecurity2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9dc0fccd-e588-4f21-b195-fb4a4cb80bb9">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes <a href="https://msdn.microsoft.com/213e555a-1509-4081-a21b-f33fc4653f32">FaxSecurity2</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
Saves the <a href="https://msdn.microsoft.com/0c1fe69c-f10b-4c7d-abe5-1a3e93d56c04">FaxSecurity</a> object data.

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

<a href="https://msdn.microsoft.com/cc2eb7bb-1b29-4cad-8061-c7d88901857b">Descriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Represents the security descriptor for a <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c7a839d9-d7d5-4942-8886-b1ca494c5842">GrantedRights</a>


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

<a href="https://msdn.microsoft.com/a9f1995e-00d1-4d20-8d3a-bf6dc80d6533">InformationType</a>


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



This interface is supported only on Windows Vista or later. For earlier versions of Windows use <a href="https://msdn.microsoft.com/e8dabda0-29aa-4ef2-a797-14aae1d8b539">IFaxSecurity</a>.

Only an administrator with permissions can configure the security of the fax server. For more information, see <a href="http://msdn.microsoft.com/library/en-us/secauthz/security/access_control.asp">Access Control</a>.

A default implementation is provided as <a href="https://msdn.microsoft.com/213e555a-1509-4081-a21b-f33fc4653f32">FaxSecurity2</a>. 



