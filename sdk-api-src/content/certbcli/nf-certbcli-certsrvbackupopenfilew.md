---
UID: NF:certbcli.CertSrvBackupOpenFileW
title: CertSrvBackupOpenFileW function
author: windows-driver-content
description: Opens a file for backup.
old-location: security\certsrvbackupopenfile.htm
old-project: SecCrypto
ms.assetid: 5ddce73f-c693-437a-9eae-d7eaf482ee05
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CertSrvBackupOpenFile, CertSrvBackupOpenFile function [Security], CertSrvBackupOpenFileW, _certsrv_certsrvbackupopenfile, certbcli/CertSrvBackupOpenFile, certbcli/CertSrvBackupOpenFileW, security.certsrvbackupopenfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: certbcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertSrvBackupOpenFileW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Certadm.dll
api_name:
-	CertSrvBackupOpenFile
-	CertSrvBackupOpenFileW
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# CertSrvBackupOpenFileW function


## -description



			The <b>CertSrvBackupOpenFile</b> function opens a file for backup.


## -parameters




### -param hbc [in]

A handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> backup context.


### -param pwszAttachmentName [in]

File name to open for backup purposes. This file name would be parsed from a list produced by means of 
<a href="https://msdn.microsoft.com/bbc6e6c2-bb2c-4b0e-b1ba-6acf26a48f45">CertSrvBackupGetBackupLogs</a> or 
<a href="https://msdn.microsoft.com/5e62be79-693a-4543-8d83-262f00686c99">CertSrvBackupGetDatabaseNames</a>. Note that the names returned by <b>CertSrvBackupGetBackupLogs</b> and <b>CertSrvBackupGetDatabaseNames</b> must have the single-WCHAR CSBFT_* prefix stripped before <b>CertSrvBackupOpenFile</b> is called.


### -param cbReadHintSize [in]

Number of bytes used as a hint when the file is read by 
<a href="https://msdn.microsoft.com/cfc72002-40ee-4854-a026-b956acd5d758">CertSrvBackupRead</a>. The <i>cbReadHintSize</i> parameter passed to the first <b>CertSrvBackupOpenFile</b> call for the backup context is used to size the read buffer. Pass zero for this parameter, and the buffer will be sized at a reasonably efficient size chosen by <b>CertSrvBackupOpenFile</b>. If insufficient memory is available, the buffer size will be reduced until memory allocation succeeds or until the buffer size reaches its minimum possible value. Pass a nonzero size to cause <b>CertSrvBackupOpenFile</b> to size the buffer to a power of two near the value of <i>cbReadHintSize</i>. The  implementation will choose only powers of two between 64 KB and 4 MB.


### -param pliFileSize [out]

A pointer to a <b>LARGE_INTEGER</b> value that represents the number of bytes in the file.


## -returns




						If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Use this function to open a file for backup purposes. When you have finished using the file, close the file by calling 
the <a href="https://msdn.microsoft.com/123933b4-5496-460d-aaaa-a494786cd638">CertSrvBackupClose</a> function.

The name of this  function in Certadm.dll is <b>CertSrvBackupOpenFileW</b>. You must use this form of the name when calling <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. Also, this function is defined as type <b>FNCERTSRVBACKUPOPENFILEW</b> in  Certbcli.h.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNCERTSRVBACKUPOPENFILEW* pfnOpenFile;
char * szBackupOpenFunc = "CertSrvBackupOpenFileW";
LARGE_INTEGER liFileSize;
HRESULT       hr=0;

// Get the address for the desired function.    
// hInst was set by calling LoadLibrary for Certadm.dll.
pfnOpenFile = (FNCERTSRVBACKUPOPENFILEW*)GetProcAddress(hInst,
                                         szBackupOpenFunc);
if ( NULL == pfnOpenFile )
{
    printf("Failed GetProcAddress - %s, error=%d\n",
            szBackupOpenFunc,
            GetLastError() );
    exit(1); // or other appropriate error action
}

// Open the file.
// hCSBC was set by an earlier call to CertSrvBackupPrepare.
// pwszFile specifies the name of a file.
// This name could have resulted from parsing the
// output from CertSrvBackupGetDatabaseNames, and so on.
hr = pfnOpenFile(hCSBC,
                pwszFile,
                0,
                &amp;liFileSize);
if (FAILED(hr))
{
    printf("Failed pfnOpenFile call [%x] %ws\n",
           hr,
           pwszFile);
           exit(1); // Or other appropriate error action.
}

// Use the opened file as needed.
// When you have finished using the file, call CertSrvBackupClose.
// ...</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/123933b4-5496-460d-aaaa-a494786cd638">CertSrvBackupClose</a>



<a href="https://msdn.microsoft.com/cfc72002-40ee-4854-a026-b956acd5d758">CertSrvBackupRead</a>



<a href="https://msdn.microsoft.com/47e8f490-ecb2-4c41-8bf0-b673e173ddc6">Using the Certificate Services Backup and Restore Functions</a>
 

 

