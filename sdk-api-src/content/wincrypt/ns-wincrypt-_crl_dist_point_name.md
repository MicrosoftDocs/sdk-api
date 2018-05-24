---
UID: NS:wincrypt._CRL_DIST_POINT_NAME
title: "_CRL_DIST_POINT_NAME"
author: windows-driver-content
description: Identifies a location from which the CRL can be obtained.
old-location: security\crl_dist_point_name.htm
old-project: SecCrypto
ms.assetid: f47283c3-34f5-4611-b041-456d28d85dbe
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: "*PCRL_DIST_POINT_NAME, CRL_DIST_POINT_FULL_NAME, CRL_DIST_POINT_ISSUER_RDN_NAME, CRL_DIST_POINT_NAME, CRL_DIST_POINT_NAME structure [Security], CRL_DIST_POINT_NO_NAME, PCRL_DIST_POINT_NAME, PCRL_DIST_POINT_NAME structure pointer [Security], _CRL_DIST_POINT_NAME, _crypto2_crl_dist_point_name, security.crl_dist_point_name, wincrypt/CRL_DIST_POINT_NAME, wincrypt/PCRL_DIST_POINT_NAME"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRL_DIST_POINT_NAME, *PCRL_DIST_POINT_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRL_DIST_POINT_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

