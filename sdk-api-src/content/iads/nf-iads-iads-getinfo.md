---
UID: NF:iads.IADs.GetInfo
title: IADs::GetInfo (iads.h)
description: Loads into the property cache values of the supported properties of this ADSI object from the underlying directory store.
helpviewer_keywords: ["GetInfo","GetInfo method [ADSI]","GetInfo method [ADSI]","IADs interface","IADs interface [ADSI]","GetInfo method","IADs.GetInfo","IADs::GetInfo","_ds_iads_getinfo","adsi.iads__getinfo","adsi.iads_getinfo","iads/IADs::GetInfo"]
old-location: adsi\iads_getinfo.htm
tech.root: adsi
ms.assetid: 73ceaeb1-9a6b-449a-9851-3756736dbad7
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [ADSI], GetInfo method [ADSI],IADs interface, IADs interface [ADSI],GetInfo method, IADs.GetInfo, IADs::GetInfo, _ds_iads_getinfo, adsi.iads__getinfo, adsi.iads_getinfo, iads/IADs::GetInfo
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
 - IADs::GetInfo
 - iads/IADs::GetInfo
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
 - IADs.GetInfo
---

# IADs::GetInfo


## -description

The <b>IADs::GetInfo</b> method loads into the property cache values of the supported properties of this ADSI object from the underlying directory store.



## -returns

This method supports the standard return values, as well as the following.
      

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The <b>IADs::GetInfo</b> function is called to initialize or refresh the property cache. This is similar to obtaining those property values of supported properties from the underlying directory store.

An uninitialized property cache is not necessarily empty. Call  <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> or  <a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs::PutEx</a> to place a value into the property cache for any supported property and the cache remains uninitialized.

An explicit call to <b>IADs::GetInfo</b> loads or reloads the entire property cache, overwriting all the cached property values. But an implicit call loads only those properties not set in the cache. Always call <b>IADs::GetInfo</b> explicitly to retrieve the most current property values of the ADSI object.

Because an explicit call to <b>IADs::GetInfo</b> overwrites all the values in the property cache, any change made to the cache will be lost if an  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> was not invoked before <b>IADs::GetInfo</b>.

For an ADSI container object, <b>IADs::GetInfo</b> caches only the property values of the container, but not those of the child objects.

It is important to emphasize the differences between the  <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> and <b>IADs::GetInfo</b> methods. The former returns values of a given property from the property cache whereas the latter loads all the supported property values into the property cache from the underlying directory store.

The following code example illustrates the differences between the <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> and <b>IADs::GetInfo</b> methods.


```vb
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
                                     ' The first IADs::Get calls
                                     ' GetInfo implicitly.
Debug.Print x.Get("homePhone")       ' Assume value is '999-9999'. 
x.Put "homePhone", "868-4449"        ' Put with no commit(SetInfo)
Debug.Print x.Get("homePhone")       ' Value='868-4449' from the cache.
x.GetInfo                            ' Refresh the cache, get the data 
                                     ' from the directory.
Debug.Print x.Get("homePhone")       ' Value will be '999-9999'.
```


For increased performance, explicitly call <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a> to refresh specific properties. Also, <b>IADs::GetInfoEx</b> 
must be called instead of <b>IADs::GetInfo</b> if the object's operational property values have to be accessed. This function overwrites any previously cached values of the specified properties.


#### Examples

The following code example uses a computer object served by the WinNT provider. The supported properties include <b>Owner</b> ("Owner"), <b>OperatingSystem</b> ("Windows NT"), <b>OperatingSystemVersion</b> ("4.0"), <b>Division</b> ("Fabrikam"), <b>ProcessorCount</b> ("Uniprococessor Free"), <b>Processor</b> ("x86 Family 6 Model 5 Stepping 1"). The default values are shown in parentheses.


```vb
Dim pList As IADsPropertyList
Dim pEntry As IADsPropertyEntry
Dim pValue As IADsPropertyValue

On Error GoTo Cleanup
 
Set pList = GetObject("WinNT://localhost,computer")
 
' pList now represents an uninitialized empty property cache.
pList.Put "Owner", "JeffSmith"  ' Property cache remains uninitialized,
                               ' but with one property value.
count = pList.PropertyCount  ' count = 1.
MsgBox "Number of property found in the property cache: " & count
 
v = pList.Get("Division")   ' pList.GetInfo is called implicitly
ShowPropertyCache           ' This will display "JeffSmith" for Owner,
                            ' "Fabrikam" for Division, "Windows NT" for
                            ' OperatingSystem, and so on.
 
pList.GetInfo                ' Refreshes the entire cache, overwriting 
                             ' "JeffSmith" for the Owner property.
ShowPropertyCache            ' This will display "Owner" for Owner,
                             ' "Fabrikam" for Division, "Windows NT" for
                             ' OperatingSystem, and so on.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pList = Nothing
    Set pEntry = Nothing
    Set pValue = Nothing

 
Private Sub ShowPropertyCache()
    For I = 0 To pList.PropertyCount-1
       Set pEntry = pList.Item(I)
       Debug.Print pEntry.Name
       For Each v In pEntry.Values
           Set pValue = v
           Debug.Print "   " & pvalue.CaseIgnoreString
       Next
    Next
End Sub
```


The following code example is a client-side script that illustrates the effect of <b>IADs::GetInfo</b> method. The supported properties include <b>Owner</b> ("Owner"), <b>OperatingSystem</b> ("Windows NT"), <b>OperatingSystemVersion</b> ("4.0"), <b>Division</b> ("Fabrikam"), <b>ProcessorCount</b> ("Uniprococessor Free"), <b>Processor</b> ("x86 Family 6 Model 5 Stepping 1"). The default values are shown in parentheses.


```vb
<html>
<body>
 <table>
    <tr>
       <td>Owner:</td>
       <td><input type=text name=txtOwner></td>
    </tr>
    <tr>
       <td>Operating System:</td>
       <td><input type=text name=txtOS></td>
    </tr>
    <tr>
       <td>Operating System Version:</td>
       <td><input type=text name=txtOSV></td>
    </tr>
    <tr>
       <td>Division:</td>
       <td><input type=text name=txtDiv></td>
    </tr>
 </table>

 <input type=button onClick = "showGetInfo()">
</body>

<script language="vbscript">
Dim pList 

sub showGetInfo()
  Set oFac = CreateObject("ADsFactory")
  path = "WinNT://Fabrikam"
  ADS_SECURE_AUTH = 1
  On Error Resume Next

' Browser security requires enabled/Prompt for "Initialize and 
' script ActiveX Controls not marked as safe"
  Set pList=oFac.OpenDSObject(path,vbNullString,vbNullString,ADS_SECURE_AUTH)
   
  ' pList now represents an uninitialized empty property cache
  pList.Put "Owner" "JeffSmith"  ' Property cache remain uninitialized
                                 ' but with one property value.
   
  v = pList.Get("Division")   ' pList.GetInfo is called implicitly
  ShowPropertyCache           ' This will display "JeffSmith" for Owner,
                              ' "Fabrikam" for Division, "Windows NT"
                              ' for OperatingSystem, and so on.
 
  pList.GetInfo                ' Refreshes entire cache, overwriting 
                               ' "JeffSmith" for the Owner property.
  ShowPropertyCache            ' This will display "Owner" for Owner,
                               ' "Fabrikam" for Division, "Windows NT"
                               ' for OperatingSystem, and so on.
end sub

sub ShowPropertyCache()
  txtOwner.value = pList.Get("Owner")
  txtDiv.value = pList.Get("Division")
  txtOS.Value = pList.Get("OperatingSystem")
  txtOSV.value = pList.Get("OperatingSystemVersion")
end sub
</script>

</html>
```


The following code example highlights the effect of Get and GetInfo. For brevity, error checking is omitted.


```cpp
IADs *pADs;
IADsPropertyList *pList;
BSTR bstr;
VARIANT var;
HRESULT hr;
 
hr = ADsGetObject(L"WinNT://somecomputer,computer",
                  IID_IADsPropertyList,
                  (void**)&pList);

if(!(hr==S_OK)){return hr;}

VariantInit(&var);
 
// Get the number of property entries, should be zero.
long pCount;      
hr = pList->get_PropertyCount(&pCount);
printf("    prop count = %d\n",pCount);     // 0 for empty cache.
 
hr = pList->QueryInterface(IID_IADs, (void**)&pADs);
 
 
// Set "Owner=JeffSmith" in the property cache.
V_BSTR(&var) = SysAllocString(L"JeffSmith");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("Owner"), var);
VariantClear(&var);
 
// This time the number of property entries should read one (1).
hr = pList->get_PropertyCount(&pCount);
printf("    prop count = %d\n",pCount);    // 1 for what was set.
 
// The following Get invokes GetInfo implicitly, but 
// the cache (that is, "Owner=JeffSmith") remains intact.
hr = pADs->Get(CComBSTR("Division"), &var);  
printf("    division   = %S\n", V_BSTR(&var));
VariantClear(&var);
 
hr = pADs->Get(CComBSTR("Owner"), &var);
printf("    owner      = %S\n", V_BSTR(&var));  // Owner = JeffSmith
VariantClear(&var);
 
// The following GetInfo call refreshes the entire prop cache.
// Now Owner is no longer "JeffSmith", but the value stored in the
// persistent store, for example, "BenSmith".
hr = pADs->GetInfo();
 
hr = pADs->Get(CComBSTR("Owner"), &var);
printf("    owner      = %S\n", V_BSTR(&var));  // Owner = BenSmith
VariantClear(&var);
 
// ...

if(pADs)
   pADs->Release();

if(pList)
   pList->Release();
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getex">IADs::GetEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/ADSI/property-cache-interfaces">Property
  Cache</a>
