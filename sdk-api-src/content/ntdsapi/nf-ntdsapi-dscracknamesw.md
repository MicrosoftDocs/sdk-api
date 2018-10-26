---
UID: NF:ntdsapi.DsCrackNamesW
title: DsCrackNamesW function
author: windows-sdk-content
description: Converts an array of directory service object names from one format to another.
old-location: ad\dscracknames.htm
tech.root: ad
ms.assetid: f812a001-5aab-4c62-87bd-54f95792e271
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DsCrackNames, DsCrackNames function [Active Directory], DsCrackNamesA, DsCrackNamesW, _glines_dscracknames, ad.dscracknames, ntdsapi/DsCrackNames, ntdsapi/DsCrackNamesA, ntdsapi/DsCrackNamesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsCrackNamesW function


## -description


The <b>DsCrackNames</b> function
  converts an array of directory service object names from one format to another. Name conversion enables client applications to map between the
  multiple names used to identify various directory service objects. For example,
  user objects can be identified by SAM account names (<i>Domain</i>\<i>UserName</i>), user
  principal name (<i>UserName</i>@<i>Domain</i>.com), or distinguished name.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function. If <i>flags</i> contains
    <a href="https://msdn.microsoft.com/f0108568-4a6a-4159-b55f-2c651c588b73">DS_NAME_FLAG_SYNTACTICAL_ONLY</a>, <i>hDS</i> can be
    <b>NULL</b>.


### -param flags [in]

Contains one or more of the <a href="https://msdn.microsoft.com/f0108568-4a6a-4159-b55f-2c651c588b73">DS_NAME_FLAGS</a> values used to determine how the name syntax will be cracked.


### -param formatOffered [in]

Contains one of the <a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_NAME_FORMAT</a> values that identifies the format of the input names.

The <b>DS_LIST_NCS</b> value can also be passed for this parameter. This causes <b>DsCrackNames</b> to return the distinguished names of all naming contexts in the current forest. The <i>formatDesired</i> parameter is ignored. <i>cNames</i> must be at least one and all strings in <i>rpNames</i> must have a length greater than zero characters. The contents of the <i>rpNames</i> strings is ignored.

<div class="alert"><b>Note</b>  <b>DS_LIST_NCS</b> is not defined in a published header file. To use this value, define it in the exact format shown below.</div>
<div> </div>

```cpp
#ifndef DS_LIST_NCS
    #define DS_LIST_NCS 0xfffffff6
#endif
```



### -param formatDesired [in]

Contains one of the <a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_NAME_FORMAT</a> values that identifies the format of the output names. The <b>DS_SID_OR_SID_HISTORY_NAME</b> value is not supported.


### -param cNames [in]

Contains the number of elements in the <i>rpNames</i> array.


### -param rpNames [in]

Pointer to an array of pointers to null-terminated strings that contain names to be converted.


### -param ppResult [out]

Pointer to a <b>PDS_NAME_RESULT</b> value that receives a <a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a> structure
    that contains the converted names. The caller must free this memory, when it is no longer required, by calling <a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>.


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
    names are reported in the <b>status</b> member of the <a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a> structure returned for each input name.

<div class="alert"><b>Note</b>  Do not confuse the values of the format elements of
    the <i>formatOffered</i> parameter used by the
    <b>DsCrackNames</b> function with the similarly
    named format elements as defined in the <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a> enumeration used by the <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> interface. The
    two sets of element formats are not equivalent and are not interchangeable.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/f0108568-4a6a-4159-b55f-2c651c588b73">DS_NAME_FLAGS</a>



<a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_NAME_FORMAT</a>



<a href="https://msdn.microsoft.com/8c3cedae-f998-482c-95db-33bca94e119b">DS_NAME_RESULT</a>



<a href="https://msdn.microsoft.com/50a4488f-e2d4-4671-b0e7-fb8cb4096c5c">DS_NAME_RESULT_ITEM</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/210650a6-70b9-4d4f-b99a-106afd3fe615">DsFreeNameResult</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>
 

 

