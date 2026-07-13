---
UID: NF:ntdsapi.DsCrackNamesW
title: DsCrackNamesW function (ntdsapi.h)
description: Converts an array of directory service object names from one format to another. (Unicode)
helpviewer_keywords: ["DsCrackNames", "DsCrackNames function [Active Directory]", "DsCrackNamesW", "_glines_dscracknames", "ad.dscracknames", "ntdsapi/DsCrackNames", "ntdsapi/DsCrackNamesW"]
old-location: ad\dscracknames.htm
tech.root: ad
ms.assetid: f812a001-5aab-4c62-87bd-54f95792e271
ms.date: 12/05/2018
ms.keywords: DsCrackNames, DsCrackNames function [Active Directory], DsCrackNamesA, DsCrackNamesW, _glines_dscracknames, ad.dscracknames, ntdsapi/DsCrackNames, ntdsapi/DsCrackNamesA, ntdsapi/DsCrackNamesW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsCrackNamesW (Unicode) and DsCrackNamesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsCrackNamesW
 - ntdsapi/DsCrackNamesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsCrackNames
 - DsCrackNamesA
 - DsCrackNamesW
---

# DsCrackNamesW function


## -description

The <b>DsCrackNames</b> function
  converts an array of directory service object names from one format to another. Name conversion enables client applications to map between the
  multiple names used to identify various directory service objects. For example,
  user objects can be identified by SAM account names (<i>Domain</i>&#92;<i>UserName</i>), user
  principal name (<i>UserName</i>@<i>Domain</i>.com), or distinguished name.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function. If <i>flags</i> contains
    <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_flags">DS_NAME_FLAG_SYNTACTICAL_ONLY</a>, <i>hDS</i> can be
    <b>NULL</b>.

### -param flags [in]

Contains one or more of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_flags">DS_NAME_FLAGS</a> values used to determine how the name syntax will be cracked.

### -param formatOffered [in]

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_format">DS_NAME_FORMAT</a> values that identifies the format of the input names.

The <b>DS_LIST_NCS</b> value can also be passed for this parameter. This causes <b>DsCrackNames</b> to return the distinguished names of all naming contexts in the current forest. The <i>formatDesired</i> parameter is ignored. <i>cNames</i> must be at least one and all strings in <i>rpNames</i> must have a length greater than zero characters. The contents of the <i>rpNames</i> strings is ignored.

<div class="alert"><b>Note</b>  <b>DS_LIST_NCS</b> is not defined in a published header file. To use this value, define it in the exact format shown below.</div>
<div> </div>

```cpp
#ifndef DS_LIST_NCS
    #define DS_LIST_NCS 0xfffffff6
#endif
```

### -param formatDesired [in]

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_format">DS_NAME_FORMAT</a> values that identifies the format of the output names. The <b>DS_SID_OR_SID_HISTORY_NAME</b> value is not supported.

### -param cNames [in]

Contains the number of elements in the <i>rpNames</i> array.

### -param rpNames [in]

Pointer to an array of pointers to null-terminated strings that contain names to be converted.

### -param ppResult [out]

Pointer to a <b>PDS_NAME_RESULT</b> value that receives a <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure
    that contains the converted names. The caller must free this memory, when it is no longer required, by calling <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>.

## -returns

Returns a Win32 error value, an RPC error value, or one of the following.

## -remarks

The success of the name conversion request depends on where the
    client is bound. Clients bind to specific instances of the directory service
    using some variant of <b>DsBind</b>. If bound to a
    global catalog, the scope of the name mapping is the entire forest. If not bound to a global catalog, the scope of the name mapping is the domain not
    covered by a global catalog for that domain controller. If not bound to a
    global catalog and a name is not found, but the input name unambiguously
    identifies its domain and this domain is in the forest, then the return data
    identifies the DNS domain name for the domain of interest. Clients are expected
    to use this data to bind to the correct domain controller or global
    catalog and call <b>DsCrackNames</b> again with the new bind handle.

The return value from <b>DsCrackNames</b> indicates errors such as invalid
    parameters or insufficient memory. However, problems in converting individual
    names are reported in the <b>status</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a> structure returned for each input name.

<div class="alert"><b>Note</b>  Do not confuse the values of the format elements of
    the <i>formatOffered</i> parameter used by the
    <b>DsCrackNames</b> function with the similarly
    named format elements as defined in the <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a> enumeration used by the <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> interface. The
    two sets of element formats are not equivalent and are not interchangeable.</div>
<div> </div>




> [!NOTE]
> The ntdsapi.h header defines DsCrackNames as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>



<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_flags">DS_NAME_FLAGS</a>



<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_name_format">DS_NAME_FORMAT</a>



<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_result_itema">DS_NAME_RESULT_ITEM</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>
