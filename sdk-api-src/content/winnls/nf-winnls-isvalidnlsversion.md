---
UID: NF:winnls.IsValidNLSVersion
title: IsValidNLSVersion function (winnls.h)
author: windows-sdk-content
description: Determines if the NLS version is valid for a given NLS function.
old-location: intl\isvalidnlsversion.htm
tech.root: Intl
ms.assetid: 29556DB4-E569-4161-9E47-149E4C12DD3B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsValidNLSVersion, IsValidNLSVersion function [Internationalization for Windows Applications], intl.isvalidnlsversion, winnls/IsValidNLSVersion
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsValidNLSVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsValidNLSVersion function


## -description


Determines if the NLS version is valid for a given NLS function.


## -parameters




### -param function [in]

The NLS capability to query. This value must be COMPARE_STRING. See the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration.


### -param lpLocaleName [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/221aae7b-3a7c-4995-ae78-50d97de436d8">locale name</a>, or one of the following predefined values. 

<ul>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_INVARIANT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63e2e368-af2f-4af0-bbea-2b27d1939394">LOCALE_NAME_USER_DEFAULT</a>
</li>
</ul>

### -param lpVersionInformation [in]

Pointer to an <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure. The application must initialize the <b>dwNLSVersionInfoSize</b> member to <code> sizeof(NLSVERSIONINFOEX)</code>. 


## -returns



Returns a nonzero value if the NLS version is valid, or zero if the version is invalid.




## -remarks



Initialize the <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> structure by calling <a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>. See the Remarks for <b>GetNLSVersionEx</b> for a discussion on how the members of <b>NLSVERSIONINFOEX</b> can be used to determine if a sort version has changed and you need to reindex data.

<b>Beginning in Windows 8:</b> If your app passes language tags to this function from the <a href="https://msdn.microsoft.com/e9e566c3-e84a-44d3-980f-fe8bbd5e052a">Windows.Globalization</a> namespace, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>
 

 

