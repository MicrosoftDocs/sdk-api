---
UID: NN:iads.IADsLargeInteger
title: IADsLargeInteger
author: windows-sdk-content
description: Used to manipulate 64-bit integers of the LargeInteger type.
old-location: adsi\iadslargeinteger.htm
old-project: ADSI
ms.assetid: d49e3339-8488-44c1-9d60-706492e65abc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsLargeInteger, IADsLargeInteger interface [ADSI], IADsLargeInteger interface [ADSI],described, _ds_iadslargeinteger, adsi.iadslargeinteger, iads/IADsLargeInteger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsLargeInteger
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsLargeInteger interface


## -description


The <b>IADsLargeInteger</b> interface is used to manipulate 64-bit integers of the <b>LargeInteger</b> type.


## -remarks



Handling the <b>IADsLargeInteger</b> in Visual Basic is made difficult by the fact that Visual Basic has no native unsigned numeric data type. This can cause errors in data conversion if either the <a href="https://msdn.microsoft.com/73e0c7fe-e468-4f92-9c9e-721bf00dd4bb">LowPart</a> or <b>HighPart</b> has the high bit set, which causes Visual Basic to handle the number as negative. The Visual Basic code examples below show how to properly handle the <b>IADsLargeInteger</b> in Visual Basic.


#### Examples

The following example shows how to convert an <b>IADsLargeInteger</b> object to a hex string.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim oDomain As IADs
Dim oLargeInt As LargeInteger

Set oDomain = GetObject("LDAP://DC=fabrikam,DC=com")
Set oLargeInt = oDomain.Get("creationTime")

Debug.Print oLargeInt.HighPart
Debug.Print oLargeInt.LowPart

strTemp = "&amp;H" + CStr(Hex(oLargeInt.HighPart)) + _
     CStr(Hex(oLargeInt.LowPart))
Debug.Print strTemp</pre>
</td>
</tr>
</table></span></div>
In Visual Basic, it is possible to convert an <b>IADsLargeInteger</b> objects that represents a date and/or time into a time Variant using the <a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a> and <a href="https://msdn.microsoft.com/d9d69521-9b33-4fc5-8a1c-929f216db450">SystemTimeToVariantTime</a> APIs. This is shown in the following code example.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Public Declare Function FileTimeToSystemTime Lib "kernel32" _
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

End Function</pre>
</td>
</tr>
</table></span></div>
The following example shows how to convert an <b>IADsLargeInteger</b> to a 64-bit integer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT PrintAccountExpires(LPCWSTR pwszADsPath)
{
    if(!pwszADsPath)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr;
    CComPtr&lt;IADs&gt; spads;

    // Bind to the object.
    hr = ADsGetObject(pwszADsPath, IID_IADs, (LPVOID*)&amp;spads);
    if(FAILED(hr))
    {
        return hr;
    }

    /*
    Get the accountExpires attribute, which is an
    IDispatch that contains an IADsLargeInteger.
    */
    CComVariant svar;
    hr = spads-&gt;Get(CComBSTR("accountExpires"), &amp;svar);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the IADsLargeInteger interface.
    CComPtr&lt;IADsLargeInteger&gt; spli;
    hr = svar.pdispVal-&gt;QueryInterface(IID_IADsLargeInteger, 
                                      (LPVOID*)&amp;spli);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the high and low parts of the value.
    long lHigh;
    long lLow;
    hr = spli-&gt;get_HighPart(&amp;lHigh);
    hr = spli-&gt;get_LowPart(&amp;lLow);

    // Convert the high and low parts to an __i64.
    __int64 i64;
    i64 = (ULONG)lHigh;
    i64 = (i64 &lt;&lt; 32);
    i64 = i64 + (ULONG)lLow;
    
    // Print all of the values.
    wprintf(L"HighPart = %u, LowPart = %u, Combined = %I64d\n", 
            lHigh, lLow, i64);

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/73e0c7fe-e468-4f92-9c9e-721bf00dd4bb">IADsLargeInteger Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

