---
UID: NF:dsclient.DsBrowseForContainerA
title: DsBrowseForContainerA function (dsclient.h)
description: Displays a dialog box used to browse for container objects in Active Directory Domain Services. (ANSI)
helpviewer_keywords: ["DsBrowseForContainer","DsBrowseForContainer function [Active Directory]","DsBrowseForContainerA","DsBrowseForContainerW","_glines_dsbrowseforcontainer","ad.dsbrowseforcontainer","dsclient/DsBrowseForContainer","dsclient/DsBrowseForContainerA","dsclient/DsBrowseForContainerW"]
old-location: ad\dsbrowseforcontainer.htm
tech.root: ad
ms.assetid: c95585b3-bf40-4aee-ae47-ca8f43daf0e6
ms.date: 12/05/2018
ms.keywords: DsBrowseForContainer, DsBrowseForContainer function [Active Directory], DsBrowseForContainerA, DsBrowseForContainerW, _glines_dsbrowseforcontainer, ad.dsbrowseforcontainer, dsclient/DsBrowseForContainer, dsclient/DsBrowseForContainerA, dsclient/DsBrowseForContainerW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsBrowseForContainerA
 - dsclient/DsBrowseForContainerA
dev_langs:
 - c++
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
---

# DsBrowseForContainerA function


## -description

The <b>DsBrowseForContainer</b> function displays a dialog box used to browse for container objects in Active Directory Domain Services.

## -parameters

### -param pInfo [in]

Pointer to a <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a> structure that contains data about  initializing the container browser dialog and receives data about the selected object.

## -returns

The function returns one of the following values.

## -remarks

The dialog box displays a container picker which is either populated with containers from a particular root or which uses trusted domains. If it uses trusted domains, it can use either the domain that the user is currently logged on to, or it can use an alternate domain specified by the application using the <b>pszRoot</b> member of the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a> structure. If the user clicks the <b>OK</b> pushbutton or double-clicks an object, <b>IDOK</b> is returned and <b>pszPath</b> contains the ADsPath of the selected object. If the user cancels the dialog box, <b>DsBrowseForContainer</b> returns <b>IDCANCEL</b>.

The <b>pszRoot</b> member contains an ADsPath, which requires the  following form.


```cpp
LDAP://fabrikam.com/CN=Users,DC=Fabrikam,DC=com
```


<b>DsBrowseForContainer</b> uses this path as the root of the tree.  The <b>pszRoot</b> member can also be used to specify a domain that has a trust with the domain that the user is logged on to, so that the user can browse the <b>Users</b> container of the alternate  domain. If the <b>pszPath</b> member contains a path, the dialog will navigate from <b>pszRoot</b> through the containers until it reaches the object specified by <b>pszPath</b>.

The <b>DsBrowseForContainer</b> function supports a callback function as specified in the <a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a> structure. The callback function can be used to filter, modify, or otherwise update the view based on selection change, and so on. For more information, see 
<a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>.

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






> [!NOTE]
> The dsclient.h header defines DsBrowseForContainer as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlobj_core/nc-shlobj_core-bffcallback">BFFCallBack</a>



<a href="/windows/desktop/api/dsclient/ns-dsclient-dsbrowseinfoa">DSBROWSEINFO</a>
