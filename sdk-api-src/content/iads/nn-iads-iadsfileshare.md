---
UID: NN:iads.IADsFileShare
title: IADsFileShare
author: windows-sdk-content
description: The IADsFileShare interface is a dual interface that inherits from IADs. It is designed for representing a published file share across the network. Call the methods on IADsFileShare to access or publish data about a file share point.
old-location: adsi\iadsfileshare.htm
old-project: ADSI
ms.assetid: 37695195-fc33-499d-98c1-ccfd190cb2f9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsFileShare, IADsFileShare interface [ADSI], IADsFileShare interface [ADSI],described, _ds_iadsfileshare, adsi.iadsfileshare, iads/IADsFileShare
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsFileShare
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsFileShare interface


## -description


The <b>IADsFileShare</b> interface is a dual interface that inherits from <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. It is designed for representing a published file share across the network. Call the methods on <b>IADsFileShare</b> to access or publish data about a file share point.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsFileShare</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsFileShare</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsFileShare</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsFileShare</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">AdsPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's ADsPath that uniquely identifies this object from all others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Class</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the object's schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5a81c42-507f-4a68-b6f4-83097bd0fa01">CurrentUserCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the current number of users connected to this share.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the description of the file share.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5a81c42-507f-4a68-b6f4-83097bd0fa01">HostComputer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the ADsPath reference to the host computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5a81c42-507f-4a68-b6f4-83097bd0fa01">MaxUserCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the maximum number of users allowed to access share at any one time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string for the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915708">Path</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the file system path to shared directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
</table> 


## -remarks



<b>IADsFileShare</b> is supported by WinNT system provider only. Using the WinNT provider, you can also bind to a FPNW share by substituting "FPNW" for "LanmanServer" in the code examples below.

To bind to a file share, using the WinNT system provider, you can explicitly bind to the file service "LanmanServer" on the host machine, and then enumerate the container to reach the file share of interest, or bind directly to the file share.


#### Examples

The following code example demonstrates how to bind to the file service and enumerate the container to display the names of the shares in that container.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim fs as IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://aComputer/LanmanServer")

For Each share In fs
    MsgBox("Share: " &amp; share.name)
Next share

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example demonstrates how to bind directly to a file share.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim fs as IADsFileShare
On Error Resume Next
Set fs = GetObject("WinNT://aComputer/LanmanServer/_file_share_name_")</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/c5a81c42-507f-4a68-b6f4-83097bd0fa01">IADsFileShare Property Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

