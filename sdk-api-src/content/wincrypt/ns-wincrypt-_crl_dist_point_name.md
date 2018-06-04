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

# _CRL_DIST_POINT_NAME structure


## -description


The <b>CRL_DIST_POINT_NAME</b> structure identifies a location from which the CRL can be obtained. When <b>CRL_DIST_POINT_NAME</b> is used, different forms of the CRL distribution point name appear in the <b>FullName</b> member of the <a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> structure. An application need not be able to process all of the name forms in the structure. It can use a distribution point if at least one name form can be processed.

If no name forms for a distribution point can be processed, an application can still use the certificate, provided requisite revocation information can be obtained from another source such as a distribution point of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority's</a> (CA's) directory entry.


## -struct-fields




### -field dwDistPointNameChoice

Indicates the variant used for the name data contained in the union. The following values are defined: 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_NO_NAME"></a><a id="crl_dist_point_no_name"></a><dl>
<dt><b>CRL_DIST_POINT_NO_NAME</b></dt>
</dl>
</td>
<td width="60%">
No distribution point name is provided.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_FULL_NAME"></a><a id="crl_dist_point_full_name"></a><dl>
<dt><b>CRL_DIST_POINT_FULL_NAME</b></dt>
</dl>
</td>
<td width="60%">
The distribution point name is in the <b>FullName</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_DIST_POINT_ISSUER_RDN_NAME"></a><a id="crl_dist_point_issuer_rdn_name"></a><dl>
<dt><b>CRL_DIST_POINT_ISSUER_RDN_NAME</b></dt>
</dl>
</td>
<td width="60%">
Currently not implemented.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.FullName

A
<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> structure containing an array of alternative names specifying the CRL distribution point in one of several different forms. One of the most common uses a URL in the form "http://…" to specify the location of the CRL.


## -see-also




<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a>



<a href="https://msdn.microsoft.com/ec7ccc54-0aaa-4c32-8aa1-dcbaf59f9991">CRL_DIST_POINT</a>
 

 

