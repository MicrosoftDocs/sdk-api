---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0020
title: "__MIDL___MIDL_itf_ads_0000_0000_0020"
author: windows-sdk-content
description: The ADS_DEREFENUM enumeration specifies the process through which aliases are dereferenced.
old-location: adsi\ads_derefenum.htm
old-project: ADSI
ms.assetid: 4cd080cc-59f9-48e8-93c1-1fccea0238ad
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADS_DEREFENUM, ADS_DEREFENUM enumeration [ADSI], ADS_DEREF_ALWAYS, ADS_DEREF_FINDING, ADS_DEREF_NEVER, ADS_DEREF_SEARCHING, __MIDL___MIDL_itf_ads_0000_0000_0020, _ds_ads_derefenum, adsi.ads__derefenum, adsi.ads_derefenum, iads/ADS_DEREFENUM, iads/ADS_DEREF_ALWAYS, iads/ADS_DEREF_FINDING, iads/ADS_DEREF_NEVER, iads/ADS_DEREF_SEARCHING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADS_DEREFENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_DEREFENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_ads_0000_0000_0020 enumeration


## -description


The <b>ADS_DEREFENUM</b> enumeration specifies the process through which aliases are dereferenced.


## -enum-fields




### -field ADS_DEREF_NEVER

Does not dereference aliases when searching or locating the base object of the search.


### -field ADS_DEREF_SEARCHING

Dereferences aliases when searching subordinates of the base object, but not when locating the base itself.


### -field ADS_DEREF_FINDING

Dereferences aliases when locating the base object of the search, but not when searching its subordinates.


### -field ADS_DEREF_ALWAYS

Dereferences aliases when both searching subordinates and locating the base object of the search.


## -remarks



The  <a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface uses these constants to set the alias dereferencing behavior. If no option is specified, the server defaults to <b>ADS_DEREF_NEVER</b>.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript applications. To use the symbolic constants, as a good programming practice, explicitly declare constants, as done here.</div>
<div> </div>

#### Examples

The following code example shows how to set the search preference for alias dereferencing. m_pSearch refers to a pointer to an object implementing the <a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_SEARCHPREF_INFO prefInfo[1];
HRESULT hr;
 
prefInfo[0].dwSearchPref   = ADS_SEARCHPREF_DEREF_ALIASES;
prefInfo[0].vValue.dwType  = ADSTYPE_INTEGER;
prefInfo[0].vValue.Integer = ADS_DEREF_ALWAYS;
hr = m_pSearch-&gt;SetSearchPreference(prefInfo, 1);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

