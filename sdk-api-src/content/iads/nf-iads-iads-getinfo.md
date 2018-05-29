---
UID: NF:iads.IADs.GetInfo
title: IADs::GetInfo
author: windows-sdk-content
description: Loads into the property cache values of the supported properties of this ADSI object from the underlying directory store.
old-location: adsi\iads_getinfo.htm
old-project: ADSI
ms.assetid: 73ceaeb1-9a6b-449a-9851-3756736dbad7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetInfo, GetInfo method [ADSI], GetInfo method [ADSI],IADs interface, IADs interface [ADSI],GetInfo method, IADs.GetInfo, IADs::GetInfo, _ds_iads_getinfo, adsi.iads__getinfo, adsi.iads_getinfo, iads/IADs::GetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADs.GetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADs::GetInfo


## -description


The <b>IADs::GetInfo</b> method loads into the property cache values of the supported properties of this ADSI object from the underlying directory store.


## -parameters






## -returns



This method supports the standard return values, as well as the following.
      

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <b>IADs::GetInfo</b> function is called to initialize or refresh the property cache. This is similar to obtaining those property values of supported properties from the underlying directory store.

An uninitialized property cache is not necessarily empty. Call  <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> or  <a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a> to place a value into the property cache for any supported property and the cache remains uninitialized.

An explicit call to <b>IADs::GetInfo</b> loads or reloads the entire property cache, overwriting all the cached property values. But an implicit call loads only those properties not set in the cache. Always call <b>IADs::GetInfo</b> explicitly to retrieve the most current property values of the ADSI object.

Because an explicit call to <b>IADs::GetInfo</b> overwrites all the values in the property cache, any change made to the cache will be lost if an  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> was not invoked before <b>IADs::GetInfo</b>.

For an ADSI container object, <b>IADs::GetInfo</b> caches only the property values of the container, but not those of the child objects.

It is important to emphasize the differences between the  <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> and <b>IADs::GetInfo</b> methods. The former returns values of a given property from the property cache whereas the latter loads all the supported property values into the property cache from the underlying directory store.

The following code example illustrates the differences between the <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> and <b>IADs::GetInfo</b> methods.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
                                     ' The first IADs::Get calls
                                     ' GetInfo implicitly.
Debug.Print x.Get("homePhone")       ' Assume value is '999-9999'. 
x.Put "homePhone", "868-4449"        ' Put with no commit(SetInfo)
Debug.Print x.Get("homePhone")       ' Value='868-4449' from the cache.
x.GetInfo                            ' Refresh the cache, get the data 
                                     ' from the directory.
Debug.Print x.Get("homePhone")       ' Value will be '999-9999'.</pre>
</td>
</tr>
</table></span></div>
For increased performance, explicitly call <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a> to refresh specific properties. Also, <b>IADs::GetInfoEx</b> 
must be called instead of <b>IADs::GetInfo</b> if the object's operational property values have to be accessed. This function overwrites any previously cached values of the specified properties.


#### Examples

The following code example uses a computer object served by the WinNT provider. The supported properties include <b>Owner</b> ("Owner"), <b>OperatingSystem</b> ("Windows NT"), <b>OperatingSystemVersion</b> ("4.0"), <b>Division</b> ("Fabrikam"), <b>ProcessorCount</b> ("Uniprococessor Free"), <b>Processor</b> ("x86 Family 6 Model 5 Stepping 1"). The default values are shown in parentheses.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim pList As IADsPropertyList
Dim pEntry As IADsPropertyEntry
Dim pValue As IADsPropertyValue

On Error GoTo Cleanup
 
Set pList = GetObject("WinNT://localhost,computer")
 
' pList now represents an uninitialized empty property cache.
pList.Put "Owner", "JeffSmith"  ' Property cache remains uninitialized,
                               ' but with one property value.
count = pList.PropertyCount  ' count = 1.
MsgBox "Number of property found in the property cache: " &amp; count
 
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
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
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
           Debug.Print "   " &amp; pvalue.CaseIgnoreString
       Next
    Next
End Sub</pre>
</td>
</tr>
</table></span></div>
The following code example is a client-side script that illustrates the effect of <b>IADs::GetInfo</b> method. The supported properties include <b>Owner</b> ("Owner"), <b>OperatingSystem</b> ("Windows NT"), <b>OperatingSystemVersion</b> ("4.0"), <b>Division</b> ("Fabrikam"), <b>ProcessorCount</b> ("Uniprococessor Free"), <b>Processor</b> ("x86 Family 6 Model 5 Stepping 1"). The default values are shown in parentheses.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;html&gt;
&lt;body&gt;
 &lt;table&gt;
    &lt;tr&gt;
       &lt;td&gt;Owner:&lt;/td&gt;
       &lt;td&gt;&lt;input type=text name=txtOwner&gt;&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
       &lt;td&gt;Operating System:&lt;/td&gt;
       &lt;td&gt;&lt;input type=text name=txtOS&gt;&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
       &lt;td&gt;Operating System Version:&lt;/td&gt;
       &lt;td&gt;&lt;input type=text name=txtOSV&gt;&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
       &lt;td&gt;Division:&lt;/td&gt;
       &lt;td&gt;&lt;input type=text name=txtDiv&gt;&lt;/td&gt;
    &lt;/tr&gt;
 &lt;/table&gt;

 &lt;input type=button onClick = "showGetInfo()"&gt;
&lt;/body&gt;

&lt;script language="vbscript"&gt;
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
&lt;/script&gt;

&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>
The following code example highlights the effect of Get and GetInfo. For brevity, error checking is omitted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pADs;
IADsPropertyList *pList;
BSTR bstr;
VARIANT var;
HRESULT hr;
 
hr = ADsGetObject(L"WinNT://somecomputer,computer",
                  IID_IADsPropertyList,
                  (void**)&amp;pList);

if(!(hr==S_OK)){return hr;}

VariantInit(&amp;var);
 
// Get the number of property entries, should be zero.
long pCount;      
hr = pList-&gt;get_PropertyCount(&amp;pCount);
printf("    prop count = %d\n",pCount);     // 0 for empty cache.
 
hr = pList-&gt;QueryInterface(IID_IADs, (void**)&amp;pADs);
 
 
// Set "Owner=JeffSmith" in the property cache.
V_BSTR(&amp;var) = SysAllocString(L"JeffSmith");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("Owner"), var);
VariantClear(&amp;var);
 
// This time the number of property entries should read one (1).
hr = pList-&gt;get_PropertyCount(&amp;pCount);
printf("    prop count = %d\n",pCount);    // 1 for what was set.
 
// The following Get invokes GetInfo implicitly, but 
// the cache (that is, "Owner=JeffSmith") remains intact.
hr = pADs-&gt;Get(CComBSTR("Division"), &amp;var);  
printf("    division   = %S\n", V_BSTR(&amp;var));
VariantClear(&amp;var);
 
hr = pADs-&gt;Get(CComBSTR("Owner"), &amp;var);
printf("    owner      = %S\n", V_BSTR(&amp;var));  // Owner = JeffSmith
VariantClear(&amp;var);
 
// The following GetInfo call refreshes the entire prop cache.
// Now Owner is no longer "JeffSmith", but the value stored in the
// persistent store, for example, "BenSmith".
hr = pADs-&gt;GetInfo();
 
hr = pADs-&gt;Get(CComBSTR("Owner"), &amp;var);
printf("    owner      = %S\n", V_BSTR(&amp;var));  // Owner = BenSmith
VariantClear(&amp;var);
 
// ...

if(pADs)
   pADs-&gt;Release();

if(pList)
   pList-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a>



<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

