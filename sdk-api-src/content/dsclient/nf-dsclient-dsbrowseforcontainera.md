---
UID: NF:dsclient.DsBrowseForContainerA
title: DsBrowseForContainerA function (dsclient.h)
description: Displays a dialog box used to browse for container objects in Active Directory Domain Services. (ANSI)
helpviewer_keywords: ["DsBrowseForContainerA", "dsclient/DsBrowseForContainerA"]
old-location: ad\dsbrowseforcontainer.htm
tech.root: ad
ms.assetid: c95585b3-bf40-4aee-ae47-ca8f43daf0e6
ms.date: 06/10/2025
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

The **DsBrowseForContainer** function displays a dialog box used to browse for container objects in Active Directory Domain Services.

## -parameters

### -param pInfo [in]

Pointer to a [DSBROWSEINFO](ns-dsclient-dsbrowseinfoa.md) structure that contains data about initializing the container browser dialog and receives data about the selected object.

## -returns

The function returns **IDOK** if the user selects a container and clicks the **OK** button, or double-clicks an object. If the user cancels the dialog box, the function returns **IDCANCEL**. If an error occurs, the function returns `-1`. Use the [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) function to retrieve extended error information.

## -remarks

The dialog box displays a container picker which is either populated with containers from a particular root or which uses trusted domains. If it uses trusted domains, it can use either the domain that the user is currently logged on to, or it can use an alternate domain specified by the application using the **pszRoot** member of the [DSBROWSEINFO](ns-dsclient-dsbrowseinfoa.md) structure. If the user clicks the **OK** button or double-clicks an object, **IDOK** is returned and **pszPath** contains the ADsPath of the selected object. If the user cancels the dialog box, **DsBrowseForContainer** returns **IDCANCEL**.

The **pszRoot** member contains an ADsPath, which must be in the following format:

```cpp
LDAP://fabrikam.com/CN=Users,DC=Fabrikam,DC=com
```

**DsBrowseForContainer** uses this path as the root of the tree. The **pszRoot** member can also be used to specify a domain that has a trust with the domain that the user is signed into, so the user can browse the **Users** container of the alternate  domain. If the **pszPath** member contains a path, the dialog will navigate from **pszRoot** through the containers until it reaches the object specified by **pszPath**.

The **DsBrowseForContainer** function supports a callback function as specified in the [DSBROWSEINFO](ns-dsclient-dsbrowseinfoa.md) structure. The callback function can be used to filter, modify, or otherwise update the view based on selection change, and so on. For more information, see 
[BFFCallBack](../shlobj_core/nc-shlobj_core-bffcallback.md).

> [!IMPORTANT]
> Beginning with Windows Server 2003, the ANSI version of this function (**DsBrowseForContainerA**) is not implemented and always returns `-1`.

#### Examples

The following code example chooses a container in the domain that the user is signed into. The view also displays all the trusted domains.

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
> The `dsclient.h` header defines **DsBrowseForContainer** as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[BFFCallBack](../shlobj_core/nc-shlobj_core-bffcallback.md)

[DSBROWSEINFO](ns-dsclient-dsbrowseinfoa.md)
