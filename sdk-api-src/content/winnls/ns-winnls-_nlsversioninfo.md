---
UID: NS:winnls._nlsversioninfo
title: "_nlsversioninfo"
author: windows-driver-content
description: Deprecated. Contains version information about an NLS capability.
old-location: intl\nlsversioninfo.htm
old-project: Intl
ms.assetid: 6afc8972-373c-4198-ac54-c2a6172b3b39
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*LPNLSVERSIONINFO, LPNLSVERSIONINFO, LPNLSVERSIONINFO structure pointer [Internationalization for Windows Applications], NLSVERSIONINFO, NLSVERSIONINFO structure [Internationalization for Windows Applications], _nlsversioninfo, _win32_NLSVERSIONINFO_str, intl.nlsversioninfo, winnls/LPNLSVERSIONINFO, winnls/NLSVERSIONINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NLSVERSIONINFO, *LPNLSVERSIONINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnls.h
api_name:
-	NLSVERSIONINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _nlsversioninfo structure


## -description



Deprecated. Contains version information about an NLS capability.



Starting with Windows 8, your app should use <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a> instead of <b>NLSVERSIONINFO</b>.


## -struct-fields




### -field dwNLSVersionInfoSize

Size, in bytes, of the structure.


### -field dwNLSVersion

NLS version. This value is used to track changes and additions to the set of code points that have the indicated capability for a particular locale. The value is locale-specific, and increments when the capability changes. For example, using the COMPARE_STRING capability defined by the <a href="https://msdn.microsoft.com/c34eb904-e264-4f7d-ac7f-4ec8cfc588b6">SYSNLS_FUNCTION</a> enumeration, the version changes if sorting weights are assigned to code points that previously had no weights defined for the locale.


### -field dwDefinedVersion

Defined version. This value is used to track changes in the repertoire of Unicode code points. The value increments when the Unicode repertoire is extended, for example, if more characters are defined.


### -field dwEffectiveId

 


### -field guidCustomVersion

 




## -remarks



Starting with Windows 8, <b>NLSVERSIONINFO</b> is deprecated. In fact, it is identical to <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>, which your app should use instead.

See Remarks for <a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>.




## -see-also




<a href="https://msdn.microsoft.com/09bc53e1-69f4-4a71-82b3-1b1b84a1b84f">GetNLSVersion</a>



<a href="https://msdn.microsoft.com/255e6774-eb70-41db-a372-8796166ee8d6">GetNLSVersionEx</a>



<a href="https://msdn.microsoft.com/c8fc32bd-02bd-4a40-a836-d9ad9f69c209">Handling Sorting in Your Applications</a>



<a href="https://msdn.microsoft.com/0beb0470-ecdc-4a24-b28c-0738e1df9d49">IsNLSDefinedString</a>



<a href="https://msdn.microsoft.com/97f637df-3e0e-4349-a617-96b7c640b19d">NLSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/75382149-7d4e-4b3e-929e-ee39bf666110">National Language Support Structures</a>
 

 

