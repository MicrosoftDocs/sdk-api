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

# IEnroll4::enumPendingRequestWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumPendingRequestWStr</b> method enumerates pending <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate requests</a> and retrieves a specified property from each.  This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param lIndex [in]

Specifies the ordinal position of the pending request whose property will be retrieved. Specify zero for the first request.


### -param lDesiredProperty [in]

Identifier for the property being retrieved. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEPR_CADNS"></a><a id="xepr_cadns"></a><dl>
<dt><b>XEPR_CADNS</b></dt>
</dl>
</td>
<td width="60%">
DNS name for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA).

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CAFRIENDLYNAME"></a><a id="xepr_cafriendlyname"></a><dl>
<dt><b>XEPR_CAFRIENDLYNAME</b></dt>
</dl>
</td>
<td width="60%">
Display name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_CANAME"></a><a id="xepr_caname"></a><dl>
<dt><b>XEPR_CANAME</b></dt>
</dl>
</td>
<td width="60%">
Name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_HASH"></a><a id="xepr_hash"></a><dl>
<dt><b>XEPR_HASH</b></dt>
</dl>
</td>
<td width="60%">
Hash value of the request.

</td>
</tr>
<tr>
<td width="40%"><a id="XEPR_REQUESTID"></a><a id="xepr_requestid"></a><dl>
<dt><b>XEPR_REQUESTID</b></dt>
</dl>
</td>
<td width="60%">
Certificate request ID.

</td>
</tr>
</table>
 


### -param ppProperty [out]

A pointer to a <b>VOID</b> that receives the value of the retrieved property.
					


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.


If the following values are specified for <i>lDesiredProperty</i>, this method returns E_NOTIMPL:

<ul>
<li>XEPR_DATE</li>
<li>XEPR_V1TEMPLATENAME</li>
<li>XEPR_V2TEMPLATEOID</li>
<li>XEPR_VERSION</li>
</ul>


If you specify any other value for <i>lDesiredProperty</i>, this method returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

