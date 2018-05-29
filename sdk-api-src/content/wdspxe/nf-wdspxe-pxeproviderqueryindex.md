---
UID: NF:wdspxe.PxeProviderQueryIndex
title: PxeProviderQueryIndex function
author: windows-sdk-content
description: Returns the index of the specified provider in the list of registered providers.
old-location: wds\pxeproviderqueryindex.htm
old-project: Wds
ms.assetid: 0b28c075-7f2e-4149-b851-21614773e942
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PxeProviderQueryIndex, PxeProviderQueryIndex function [Windows Deployment Services], wds.pxeproviderqueryindex, wdspxe/PxeProviderQueryIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WdsPxe.dll
api_name:
-	PxeProviderQueryIndex
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeProviderQueryIndex function


## -description


Returns the index of the specified provider in the list of registered providers.


## -parameters




### -param pszProviderName [in]

Friendly name for the provider from the call to the 
      <a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a> function.


### -param puIndex [out]

Address of a <b>ULONG</b> that will receive the index of the provider.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



If a provider wants to insert itself in the list of registered providers in a specific order (that is, wants to 
    service client requests before or after a certain provider), it can query the index of another provider and then use 
    the returned index to decide its own location.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
// Suppose Provider wants to handle requests after BINLSVC has rejected them.
//
dwError = PxeProviderQueryIndex(L"BINLSVC", &amp;Index);

if (dwError == ERROR_SUCCESS)
{
 if (PxeProviderRegister(L"MYPROV",
                         L"C:\\MyDir\\MyProv.DLL",
                         PXE_REG_INDEX_BOTTOM,
                         Index + 1,              // Add after BINLSVC
                         &amp;hKey) != ERROR_SUCCESS)
 {
  // Handle Error
 }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

