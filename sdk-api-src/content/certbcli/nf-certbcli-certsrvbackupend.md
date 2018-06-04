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

# CertSrvBackupEnd function


## -description



			The <b>CertSrvBackupEnd</b> function ends a Certificate Services backup session.


## -parameters




### -param hbc [in]

A handle to a Certificate Services backup context.


## -returns




						The return value is an <b>HRESULT</b>. A value of S_OK indicates success.




## -remarks



Upon completion of a backup session, the session needs to be terminated by means of <b>CertSrvBackupEnd</b>. For every successful call to <a href="https://msdn.microsoft.com/21af96f8-168d-4c6c-8966-357236c0e4e6">CertSrvBackupPrepare</a>, there should be a call to <b>CertSrvBackupEnd</b>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPEND* pfnBackupEnd;
char * szBackEndFunc = "CertSrvBackupEnd";
HRESULT    hr=0;

// Get the address for the desired function.
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnBackupEnd = (FNCERTSRVBACKUPEND*)GetProcAddress(hInst,
                                       szBackEndFunc);
if (NULL == pfnBackupEnd)
{
    printf("Failed GetProcAddress - %s, error=%d\n",
           szBackEndFunc,
           GetLastError() );
    exit(1);  // Or other appropriate error action.
}

// When done, release the HCSBC.
// hCSBC would have been created by an earlier call
// to CertSrvBackupPrepare.
hr = pfnBackupEnd(hCSBC);
if (FAILED(hr))
{
    printf("Failed pfnBackupEnd call [%x]\n", hr);
    exit(1);  // Or other appropriate error action.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/21af96f8-168d-4c6c-8966-357236c0e4e6">CertSrvBackupPrepare</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

