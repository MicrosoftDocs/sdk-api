---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PeerIdentityImport function


## -description



      The <b>PeerIdentityImport</b> function imports  one peer  identity. If the peer identity exists on a computer, <b>PEER_E_ALREADY_EXISTS</b> is returned. 


## -parameters




### -param pwzImportXML [in]

Pointer to the XML format peer identity to import, which is returned by <a href="https://msdn.microsoft.com/2b7cfc46-77f6-49cb-966c-0a96830c96fd">PeerIdentityExport</a>. This binary data must match the exported data byte-for-byte.  The XML must remain valid XML with no extra 
characters.


### -param pwzPassword [in]

Specifies the password to use to de-crypt a peer identity. The password must be identical to the password supplied to <a href="https://msdn.microsoft.com/2b7cfc46-77f6-49cb-966c-0a96830c96fd">PeerIdentityExport</a>. This parameter cannot be <b>NULL</b>.


### -param ppwzIdentity [out]

Pointer to a string that represents a peer identity that is imported.  If the import operation is successful, the application must free <i>ppwzIdentity</i> by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>. 


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid, or the XML data in <i>ppwzImportXML</i> has been tampered with.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The peer identity already exists on this computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually.

</td>
</tr>
</table>
 




## -remarks



The XML fragment used by <b>PeerIdentityImport</b> is as follows:

<pre class="syntax" xml:space="preserve"><code>&lt;PEERIDENTITYEXPORT VERSION="1.0"&gt;
   &lt;IDENTITY&gt;
     &lt;!-- UTF-8 encoded peer name of the identity --&gt;
   &lt;/IDENTITY&gt;
   &lt;IDENTITYDATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64"&gt;
      &lt;!-- base64 encoded / PFX encoded and encrypted IDC with the private key --&gt;
   &lt;/IDENTTYDATA&gt;
&lt;/PEERIDENTITYEXPORT&gt;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">
        PEER_DATA</a>



<a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>



<a href="https://msdn.microsoft.com/2b7cfc46-77f6-49cb-966c-0a96830c96fd">PeerIdentityExport</a>
 

 

