---
UID: NF:aclui.ISecurityInformation2.LookupSids
title: ISecurityInformation2::LookupSids (aclui.h)
author: windows-sdk-content
description: The LookupSids method returns the common names corresponding to each of the elements in the specified list of SIDs.
old-location: security\isecurityinformation2_lookupsids.htm
tech.root: SecAuthZ
ms.assetid: 9a4056c6-6a21-4051-b4a6-c77351fce983
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISecurityInformation2 interface [Security],LookupSids method, ISecurityInformation2.LookupSids, ISecurityInformation2::LookupSids, LookupSids, LookupSids method [Security], LookupSids method [Security],ISecurityInformation2 interface, _win32_isecurityinformation2_lookupsids, aclui/ISecurityInformation2::LookupSids, security.isecurityinformation2_lookupsids
ms.topic: method
req.header: aclui.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - ISecurityInformation2.LookupSids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISecurityInformation2::LookupSids


## -description


The <b>LookupSids</b> method returns the common names corresponding to each of the elements in the specified list of SIDs.


## -parameters




### -param cSids [in]

The number of 
pointers to  <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structures pointed to by <i>rgpSids</i>.


### -param rgpSids [in]

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structures.


### -param ppdo [out]

A pointer to a pointer to a returned data transfer object that contains the common names of the SIDs. Optionally, this parameter also returns the user principal name (UPN) of the SIDs in the <i>rgpSids</i> parameter. The data transfer object is a 
<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a> structure.


## -returns



Returns S_OK if successful.
						

Returns a nonzero error code if an error occurs.




## -remarks



Your implementation of <b>LookupSids</b> can return E_NOTIMPL if the access control editor is to determine the common names corresponding to the specified SIDs. However, if the access control editor receives any return code other than S_OK, the editor determines this information.

The client must return the common names through the data object using the following format.


```cpp
#include <windows.h>

// HGLOBAL containing SID_INFO_LIST returned by
// ISecurityInformation2::LookupSids
#define CFSTR_ACLUI_SID_INFO_LIST   TEXT("CFSTR_ACLUI_SID_INFO_LIST")

// Data structures corresponding to CFSTR_ACLUI_SID_INFO_LIST
typedef struct _SID_INFO
{
    PSID    pSid;
    PWSTR   pwzCommonName;
    PWSTR   pwzClass;       // Used for selecting icon, for example,
                            // "User" or "Group"
    PWSTR   pwzUPN;         // Optional pointer to a user principal
                            // name
} SID_INFO, *PSID_INFO;

typedef struct _SID_INFO_LIST
{
    ULONG       cItems;
    SID_INFO    aSidInfo[ANYSIZE_ARRAY];
} SID_INFO_LIST, *PSID_INFO_LIST;

```





## -see-also




<a href="https://msdn.microsoft.com/ca709f27-8463-4f11-92ac-2148796e640a">Access Control Editor</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Access Control Editor Functions</a>



<a href="https://msdn.microsoft.com/5cb7a096-5088-424a-82d1-0351ce5bb413">ISecurityInformation2</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/6a69e5b9-ab6a-4bbb-9f1a-5882d4c8038c">SID_INFO</a>



<a href="https://msdn.microsoft.com/e9be644c-ec56-4a49-9aa8-6b3f62d6cf0d">SID_INFO_LIST</a>
 

 

