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

# PeerGroupImportConfig function


## -description


The <b>PeerGroupImportConfig</b> function imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.


## -parameters




### -param pwzXML [in]

Specifies a Unicode string that contains a previously exported (using <a href="https://msdn.microsoft.com/95fe1336-4bf2-4a4b-a451-90f2ae2639c2">PeerGroupExportConfig</a>) peer group configuration. For the specific XML format of the  string, see to the Remarks section of this topic. This parameter is required.


### -param pwzPassword [in]

Specifies the password used to access  the encrypted peer group configuration data, as a Unicode string. This parameter is required.


### -param fOverwrite [in]

If true, the existing group configuration is overwritten. If false, the group configuration is written only if a previous group configuration does not exist. The default value is false. This parameter is required.


### -param ppwzIdentity [out]

Contains the peer identity returned after an import completes. This parameter is required.


### -param ppwzGroup [out]

Contains a peer group peer name returned after an import completes. This parameter is required.


## -returns



Returns <b>S_OK</b> if the function succeeds. Otherwise, the function returns one of the following values.

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
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A peer group configuration already exists, and <i>fOverwrite</i> is set to false.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



To generate a peer group configuration, call <a href="https://msdn.microsoft.com/95fe1336-4bf2-4a4b-a451-90f2ae2639c2">PeerGroupExportConfig</a>, pass in an identity to export,  a password, and a handle to the peer group.

The configuration XML string appears in the following format:

<pre class="syntax" xml:space="preserve"><code>&lt;PEERGROUPCONFIG VERSION="1.0"&gt;
  &lt;IDENTITYPEERNAME&gt;
    &lt;!-- UTF-8 encoded peer name of the identity --&gt;
  &lt;/IDENTITYPEERNAME&gt;
  &lt;GROUPPEERNAME&gt;
    &lt;!-- UTF-8 encoded peer name of the peer group --&gt;
  &lt;/GROUPPEERNAME&gt;
  &lt;CLOUDNAME&gt;
    &lt;!-- UTF-8 encoded Unicode name of the cloud --&gt;
  &lt;/CLOUDNAME&gt;
  &lt;SCOPE&gt;
    &lt;!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local --&gt;
  &lt;/SCOPE&gt;
  &lt;CLOUDFLAGS&gt;
    &lt;!-- A DWORD that contains cloud-specific settings, represented as a string --&gt;
  &lt;/CLOUDFLAGS&gt;
  &lt;GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64"&gt;
    &lt;!-- base64/PKCS7 encoded GMC chain --&gt;
  &lt;/GMC&gt;
&lt;/PEERGROUPCONFIG&gt;</code></pre>


