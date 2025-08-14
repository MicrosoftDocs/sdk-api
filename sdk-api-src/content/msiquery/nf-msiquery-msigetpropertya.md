---
UID: NF:msiquery.MsiGetPropertyA
title: MsiGetPropertyA function (msiquery.h)
description: The MsiGetProperty function gets the value for an installer property. (ANSI)
helpviewer_keywords: ["MsiGetPropertyA", "msiquery/MsiGetPropertyA"]
old-location: setup\msigetproperty.htm
tech.root: setup
ms.assetid: f2844673-3440-4b43-a9d0-31b9e8086f6f
ms.date: 12/05/2018
ms.keywords: MsiGetProperty, MsiGetProperty function, MsiGetPropertyA, MsiGetPropertyW, _msi_msigetproperty, msiquery/MsiGetProperty, msiquery/MsiGetPropertyA, msiquery/MsiGetPropertyW, setup.msigetproperty
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetPropertyW (Unicode) and MsiGetPropertyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiGetPropertyA
 - msiquery/MsiGetPropertyA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiGetProperty
 - MsiGetPropertyA
 - MsiGetPropertyW
---

# MsiGetPropertyA function


## -description

The 
<b>MsiGetProperty</b> function gets the value for an installer property.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szName [in]

A null-terminated string that specifies the name of the property.

### -param szValueBuf [out]

Pointer to the buffer that receives the null terminated string containing the value of the property. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szValueBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function will then return ERROR_MORE_DATA and <i>pchValueBuf </i> will contain the required buffer size in TCHARs, not including the terminating null character. On return of ERROR_SUCCESS, <i>pcchValueBuf </i> contains the number of TCHARs written to the buffer, not including the terminating null character.

### -param pcchValueBuf [in, out]

Pointer to the variable that specifies the size, in TCHARs, of the buffer pointed to by the variable <i>szValueBuf</i>. When the function returns ERROR_SUCCESS, this variable contains the size of the data copied to <i>szValueBuf</i>, not including the terminating null character. If <i>szValueBuf </i> is not large enough, the function returns ERROR_MORE_DATA and stores the required size, not including the terminating null character, in the variable pointed to by <i>pchValueBuf</i>.

## -returns

This function returns UINT.

## -remarks

If the value for the property retrieved by the 
<b>MsiGetProperty</b> function is not defined, it is equivalent to a 0-length value. It is not an error.

If ERROR_MORE_DATA is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If ERROR_SUCCESS is returned, it gives the number of characters written to the string buffer. Therefore you can get the size of the buffer by passing in an empty string (for example "") for the parameter that specifies the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).

The following example shows how a DLL custom action could access the value of a property by dynamically determining the size of the value buffer.


```cpp
UINT __stdcall MyCustomAction(MSIHANDLE hInstall)
{
    TCHAR* szValueBuf = NULL;
    DWORD cchValueBuf = 0;
    UINT uiStat =  MsiGetProperty(hInstall, TEXT("MyProperty"), TEXT(""), &cchValueBuf);
    //cchValueBuf now contains the size of the property's string, without null termination
    if (ERROR_MORE_DATA == uiStat)
    {
        ++cchValueBuf; // add 1 for null termination
        szValueBuf = new TCHAR[cchValueBuf];
        if (szValueBuf)
        {
            uiStat = MsiGetProperty(hInstall, TEXT("MyProperty"), szValueBuf, &cchValueBuf);
        }
    }
    if (ERROR_SUCCESS != uiStat)
    {
        if (szValueBuf != NULL) 
           delete[] szValueBuf;
        return ERROR_INSTALL_FAILURE;
    }

    // custom action uses MyProperty
    // ...

    delete[] szValueBuf;

    return ERROR_SUCCESS;
}

```






> [!NOTE]
> The msiquery.h header defines MsiGetProperty as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer State Access Functions</a>



<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>
