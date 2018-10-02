---
UID: NF:dsclient.DsBrowseForContainerW
title: DsBrowseForContainerW function
author: windows-sdk-content
description: Displays a dialog box used to browse for container objects in Active Directory Domain Services.
old-location: ad\dsbrowseforcontainer.htm
tech.root: AD
ms.assetid: c95585b3-bf40-4aee-ae47-ca8f43daf0e6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DsBrowseForContainer, DsBrowseForContainer function [Active Directory], DsBrowseForContainerA, DsBrowseForContainerW, _glines_dsbrowseforcontainer, ad.dsbrowseforcontainer, dsclient/DsBrowseForContainer, dsclient/DsBrowseForContainerA, dsclient/DsBrowseForContainerW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBrowseForContainerW (Unicode) and DsBrowseForContainerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dsuiext.lib
req.dll: Dsuiext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsuiext.dll
api_name:
 - DsBrowseForContainer
 - DsBrowseForContainerA
 - DsBrowseForContainerW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsBrowseForContainerW function


## -description


The <b>DsBrowseForContainer</b> function displays a dialog box used to browse for container objects in Active Directory Domain Services.


## -parameters




### -param pInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/eaa2da41-1ddf-42d3-b721-6649ad49acf1">DSBROWSEINFO</a> structure that contains data about  initializing the container browser dialog and receives data about the selected object.


## -returns



The function returns one of the following values.




## -remarks



The dialog box displays a container picker which is either populated with containers from a particular root or which uses trusted domains. If it uses trusted domains, it can use either the domain that the user is currently logged on to, or it can use an alternate domain specified by the application using the <b>pszRoot</b> member of the <a href="https://msdn.microsoft.com/eaa2da41-1ddf-42d3-b721-6649ad49acf1">DSBROWSEINFO</a> structure. If the user clicks the <b>OK</b> pushbutton or double-clicks an object, <b>IDOK</b> is returned and <b>pszPath</b> contains the ADsPath of the selected object. If the user cancels the dialog box, <b>DsBrowseForContainer</b> returns <b>IDCANCEL</b>.

The <b>pszRoot</b> member contains an ADsPath, which requires the  following form.


```cpp
LDAP://fabrikam.com/CN=Users,DC=Fabrikam,DC=com
```


<b>DsBrowseForContainer</b> uses this path as the root of the tree.  The <b>pszRoot</b> member can also be used to specify a domain that has a trust with the domain that the user is logged on to, so that the user can browse the <b>Users</b> container of the alternate  domain. If the <b>pszPath</b> member contains a path, the dialog will navigate from <b>pszRoot</b> through the containers until it reaches the object specified by <b>pszPath</b>.

The <b>DsBrowseForContainer</b> function supports a callback function as specified in the <a href="https://msdn.microsoft.com/eaa2da41-1ddf-42d3-b721-6649ad49acf1">DSBROWSEINFO</a> structure. The callback function can be used to filter, modify, or otherwise update the view based on selection change, and so on. For more information, see 
<a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a>.

<div class="alert"><b>Important</b>  Beginning with Windows Server 2003, the ANSI version of this function (<b>DsBrowseForContainerA</b>) is not implemented and always returns -1.</div>
<div> </div>

#### Examples

The following code example chooses a container in the domain that the user is logged on to. The view also displays all the trusted domains.


```cpp
void PickContainer(void)
{
    DSBROWSEINFOW dsbi = { 0 };
    WCHAR wszResult[MAX_PATH];
 
    dsbi.cbStruct = sizeof(dsbi);
    dsbi.pszCaption = L"The container picker";
    dsbi.pszTitle = L"Pick a container for this example.";
    dsbi.pszPath = wszResult;
    dsbi.cchPath = MAX_PATH;
    dsbi.dwFlags = DSBI_ENTIREDIRECTORY;

    int nReturn = DsBrowseForContainerW(&dsbi);
 
    if ( IDOK == nReturn )
    {
        // wszResult contains the resulting path
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/91cfef29-3e0a-4dd0-be1a-215827c23143">BFFCallBack</a>



<a href="https://msdn.microsoft.com/eaa2da41-1ddf-42d3-b721-6649ad49acf1">DSBROWSEINFO</a>
 

 

