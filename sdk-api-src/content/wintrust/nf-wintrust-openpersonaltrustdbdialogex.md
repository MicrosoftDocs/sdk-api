---
UID: NF:wintrust.OpenPersonalTrustDBDialogEx
title: OpenPersonalTrustDBDialogEx function
author: windows-driver-content
description: Displays the Certificates dialog box.
old-location: security\openpersonaltrustdbdialogex.htm
old-project: SecCrypto
ms.assetid: 5e4dbccd-4cd0-4525-85dc-3327a5b713a1
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: OpenPersonalTrustDBDialogEx, OpenPersonalTrustDBDialogEx function [Security], WT_TRUSTDBDIALOG_ONLY_PUB_TAB_FLAG, security.openpersonaltrustdbdialogex, wintrust/OpenPersonalTrustDBDialogEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wintrust.h
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
req.typenames: TEB, *PTEB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wintrust.dll
api_name:
-	OpenPersonalTrustDBDialogEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Wintrust.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenPersonalTrustDBDialogEx function


## -description


The <b>OpenPersonalTrustDBDialogEx</b> function displays the <b>Certificates</b> dialog box.
<div class="alert"><b>Note</b>  This function has no associated header file or import library. You must define the function yourself and use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters




### -param hwndParent [in, optional]

The handle of the parent window for the dialog box. If this parameter is <b>NULL</b>, the dialog box has no parent.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WT_TRUSTDBDIALOG_ONLY_PUB_TAB_FLAG"></a><a id="wt_trustdbdialog_only_pub_tab_flag"></a><dl>
<dt><b>WT_TRUSTDBDIALOG_ONLY_PUB_TAB_FLAG</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
Only display the          <b>Trusted Publisher</b> tab. By default, all of the user interface tabs are displayed and the <b>Trusted Publisher</b> tab is initially selected.

</td>
</tr>
</table>
 


### -param pvReserved [in, out, optional]

Not used. Must be <b>NULL</b>.


## -returns



Returns nonzero if the dialog box was opened successfully or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/25f1d012-0c82-4992-b924-b539d4c6dc5f">OpenPersonalTrustDBDialog</a>
 

 

