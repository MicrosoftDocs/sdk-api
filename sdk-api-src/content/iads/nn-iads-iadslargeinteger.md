---
UID: NN:iads.IADsLargeInteger
title: IADsLargeInteger (iads.h)
description: Used to manipulate 64-bit integers of the LargeInteger type.
helpviewer_keywords: ["IADsLargeInteger","IADsLargeInteger interface [ADSI]","IADsLargeInteger interface [ADSI]","described","_ds_iadslargeinteger","adsi.iadslargeinteger","iads/IADsLargeInteger"]
old-location: adsi\iadslargeinteger.htm
tech.root: adsi
ms.assetid: d49e3339-8488-44c1-9d60-706492e65abc
ms.date: 12/05/2018
ms.keywords: IADsLargeInteger, IADsLargeInteger interface [ADSI], IADsLargeInteger interface [ADSI],described, _ds_iadslargeinteger, adsi.iadslargeinteger, iads/IADsLargeInteger
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsLargeInteger
 - iads/IADsLargeInteger
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsLargeInteger
---

# IADsLargeInteger interface


## -description

The <b>IADsLargeInteger</b> interface is used to manipulate 64-bit integers of the <b>LargeInteger</b> type.

## -remarks

Handling the <b>IADsLargeInteger</b> in Visual Basic is made difficult by the fact that Visual Basic has no native unsigned numeric data type. This can cause errors in data conversion if either the <a href="/windows/desktop/ADSI/iadslargeinteger-property-methods">LowPart</a> or <b>HighPart</b> has the high bit set, which causes Visual Basic to handle the number as negative. The Visual Basic code examples below show how to properly handle the <b>IADsLargeInteger</b> in Visual Basic.


#### Examples

The following example shows how to convert an <b>IADsLargeInteger</b> object to a hex string.


```vb
Dim oDomain As IADs
Dim oLargeInt As LargeInteger

Set oDomain = GetObject("LDAP://DC=fabrikam,DC=com")
Set oLargeInt = oDomain.Get("creationTime")

Debug.Print oLargeInt.HighPart
Debug.Print oLargeInt.LowPart

strTemp = "&H" + CStr(Hex(oLargeInt.HighPart)) + _
     CStr(Hex(oLargeInt.LowPart))
Debug.Print strTemp
```


In Visual Basic, it is possible to convert an <b>IADsLargeInteger</b> objects that represents a date and/or time into a time Variant using the <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-filetimetosystemtime">FileTimeToSystemTime</a> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-systemtimetovarianttime">SystemTimeToVariantTime</a> APIs. This is shown in the following code example.


```vb
Public Declare Function FileTimeToSystemTime Lib "kernel32" _
   (lpFileTime As FILETIME, _
   lpSystemTime As SYSTEMTIME) As Long

Public Declare Function SystemTimeToVariantTime Lib "oleaut32.dll" _
    (lpSystemTime As SYSTEMTIME, _
    dbTime As Double) As Long

Public Type SYSTEMTIME
    wYear As Integer
    wMonth As Integer
    wDayOfWeek As Integer
    wDay As Integer
    wHour As Integer
    wMinute As Integer
    wSecond As Integer
    wMilliseconds As Integer
End Type

Public Type FILETIME
    dwLowDateTime As Long
    dwHighDateTime As Long
End Type


' This function will convert the ADSI data type LargeInteger to
' a Variant time value in Greenwich Mean Time (GMT).
Function LargeInteger_To_Time(oLargeInt As LargeInteger, vTime As Variant)_
              As Boolean
    On Error Resume Next
    Dim pFileTime As FILETIME
    Dim pSysTime As SYSTEMTIME
    Dim dbTime As Double
    Dim lResult As Long
    
    If (oLargeInt.HighPart = 0 And oLargeInt.LowPart = 0) Then
        vTime = 0
        LargeInteger_To_Time = True
        Exit Function
    End If
    
    If (oLargeInt.LowPart = -1) Then
        vTime = -1
        LargeInteger_To_Time = True
        Exit Function
    End If
    
    pFileTime.dwHighDateTime = oLargeInt.HighPart
    pFileTime.dwLowDateTime = oLargeInt.LowPart
    
    ' Convert the FileTime to System time.
    lResult = FileTimeToSystemTime(pFileTime, pSysTime)
    If lResult = 0 Then
        LargeInteger_To_Time = False
        Debug.Print "FileTimeToSystemTime: " + Err.Number + "  - "_
                   + Err.Description
        Exit Function
    End If
    
    ' Convert System Time to a Double.
    lResult = SystemTimeToVariantTime(pSysTime, dbTime)
    If lResult = 0 Then
        LargeInteger_To_Time = False
        Debug.Print "SystemTimeToVariantTime: " + Err.Number + _
                 "  - " + Err.Description
        Exit Function
    End If
    
    ' Place the double in the variant.
    vTime = CDate(dbTime)
    LargeInteger_To_Time = True

End Function
```


The following example shows how to convert an <b>IADsLargeInteger</b> to a 64-bit integer.


```cpp
HRESULT PrintAccountExpires(LPCWSTR pwszADsPath)
{
    if(!pwszADsPath)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    CComPtr<IADs> spads;

    // Bind to the object.
    hr = ADsGetObject(pwszADsPath, IID_IADs, (LPVOID*)&spads);
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    Get the accountExpires attribute, which is an
    IDispatch that contains an IADsLargeInteger.
    */
    CComVariant svar;
    hr = spads->Get(CComBSTR("accountExpires"), &svar);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the IADsLargeInteger interface.
    CComPtr<IADsLargeInteger> spli;
    hr = svar.pdispVal->QueryInterface(IID_IADsLargeInteger, 
                                      (LPVOID*)&spli);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the high and low parts of the value.
    long lHigh;
    long lLow;
    hr = spli->get_HighPart(&lHigh);
    hr = spli->get_LowPart(&lLow);

    // Convert the high and low parts to an __i64.
    __int64 i64;
    i64 = (ULONG)lHigh;
    i64 = (i64 << 32);
    i64 = i64 + (ULONG)lLow;
    
    // Print all of the values.
    wprintf(L"HighPart = %u, LowPart = %u, Combined = %I64d\n", 
            lHigh, lLow, i64);

    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/iadslargeinteger-property-methods">IADsLargeInteger Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>