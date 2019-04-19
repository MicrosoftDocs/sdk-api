---
UID: NF:certadm.ICertAdmin2.SetConfigEntry
title: ICertAdmin2::SetConfigEntry (certadm.h)
author: windows-sdk-content
description: Sets configuration information for a certification authority (CA).
old-location: security\icertadmin2_setconfigentry.htm
tech.root: SecCrypto
ms.assetid: 6ed1dd69-3553-4dcc-a98a-1954013082cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertAdmin2 interface [Security],SetConfigEntry method, ICertAdmin2.SetConfigEntry, ICertAdmin2::SetConfigEntry, SetConfigEntry, SetConfigEntry method [Security], SetConfigEntry method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::SetConfigEntry, security.icertadmin2_setconfigentry
ms.topic: method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.SetConfigEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertAdmin2::SetConfigEntry


## -description


The <b>SetConfigEntry</b> method sets configuration  information for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA).


## -parameters




### -param strConfig [in]

String value that represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>. This parameter can be an empty string, in which case the function sets configuration information that is not specific to a CA. This parameter cannot be <b>NULL</b>.

<div class="alert"><b>Important</b>  <b>SetConfigEntry</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param strNodePath [in]

String value that represents the node path for the configuration information. This parameter can be an empty string, in which case the function retrieves configuration information from the path identified by <i>strConfig</i>. This parameter cannot be <b>NULL</b>.


### -param strEntryName [in]

String value that represents the name of the entry whose information is being set. This value can be an empty string, in which case the default entry  is the entry being set. This parameter cannot be <b>NULL</b>.


### -param pvarEntry [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>Pointer to <b>VARIANT</b> that specifies the information to set. If this value is empty, then the indicated key will be deleted.</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td><b>Variant</b> that specifies the information to set. If this value is empty, then the indicated key will be deleted.</td>
</tr>
</table>

## -returns



<h3>VB</h3>
If the function is successful, the return value is S_OK.

 
If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



 The configuration information is stored in the registry under the following path.


<b>HKEY_LOCAL_MACHINE</b>\<b>SYSTEM</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>CertSvc</b>\<b>Configuration</b>\<i>[CASANITIZEDNAME]</i>\<i>[strNodePath]</i>\<i>[strEntryName]</i></p>Where <i>CASANITIZEDNAME</i> is the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">sanitized name</a> for the CA. For more information about sanitized names, see <a href="https://msdn.microsoft.com/3a35b2a0-f8e4-496d-b76a-a7310842cc4c">ICertConfig2::GetConfig</a>.




## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>
 

 

