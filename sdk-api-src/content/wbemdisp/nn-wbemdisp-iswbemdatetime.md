---
UID: NN:wbemdisp.ISWbemDateTime
title: ISWbemDateTime
author: windows-sdk-content
description: The SWbemDateTime object is a helper object to parse and set Common Information Model (CIM) datetime values.
old-location: wmi\swbemdatetime.htm
old-project: WmiSdk
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemDateTime, SWbemDateTime, SWbemDateTime object [Windows Management Instrumentation], SWbemDateTime object [Windows Management Instrumentation],described, _hmm_swbemdatetime, wbemdisp/SWbemDateTime, wmi.swbemdatetime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemDateTime
 - ISWbemDateTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemDateTime interface


## -description


The <b>SWbemDateTime</b> object is a helper object to parse and 
    set Common Information Model (CIM) <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> values. It plays a role 
    similar to <a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>, which provides assistance to 
    format and interpret object paths. You can use  the VBScript 
    <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> call to create 
    the <b>SWbemDateTime</b> object.

An <b>SWbemDateTime</b> object can be initialized from and 
    formatted in either <b>VT_DATE</b> or <b>FILETIME</b> values using 
    methods on the object. Using properties of the object, the value can be parsed into component year, month, day, 
    hour, minutes, seconds, or microseconds. The <b>SWbemDateTime</b> 
    object can be formatted into either local or Coordinated Universal Time (UTC) values. For more information, see 
    <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.

<b>SWbemDateTime</b> is the only Windows Management 
    Instrumentation (WMI) scripting object that is marked safe for initialization  and  scripts running on HTML pages 
    in Internet Explorer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemDateTime</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemDateTime</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e0761d-e735-454a-8429-2bd1eb331123">GetFileTime</a>
</td>
<td align="left" width="63%">
Converts a <b>FILETIME</b> date and time, expressed as a 
     <b>BSTR</b>, to a WMI <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b">GetVarDate</a>
</td>
<td align="left" width="63%">
Converts a WMI <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> formatted date and time value to a 
     <b>VT_DATE</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e375afda-5e94-46d6-b1ac-e801e0f4a620">SetFileTime</a>
</td>
<td align="left" width="63%">
Converts a WMI <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a> format to a 
     <b>FILETIME</b> date and time, expressed as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24c39d44-22ac-44ac-9e05-72a5b666ab19">SetVarDate</a>
</td>
<td align="left" width="63%">
Converts a <b>VT_DATE</b> formatted date and time to a WMI 
     <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemDateTime</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60da99bc-560c-45bc-b787-f4bef8e5a509">Day</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The day component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a713378b-3953-49d8-9c6a-44aa9337eae2">DaySpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the day is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83f084fa-57a5-4467-acea-7e19de82a91f">Hours</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The hours of the day component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/55211da6-cbd5-4e61-ab7d-ee20363e9d81">HoursSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the hour is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates that at least one component of the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> 
     represents an interval rather than a date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b810b781-86a3-4730-8114-44d10454f7c3">Microseconds</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The microseconds component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/65244ece-2326-4edc-b982-57e2046ec33e">MicrosecondsSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the microseconds component is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a52a66c2-f7ab-48d0-bdee-a07984ed3bc2">Minutes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The minutes component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/de15f87e-0092-467e-b0d7-42ef447fa00a">MinutesSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the minutes component is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c">Month</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The month component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/12dd94de-24be-4b13-bde5-2fc28be94efa">MonthSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the month is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/194d4309-6abf-4c5f-99f8-60d2c835af6c">Seconds</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The seconds component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f9b75c3-ae08-49a6-b747-294831601a62">SecondsSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the seconds component is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43d9d0c8-5521-410f-825b-6b00c3dd0039">UTC</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The UTC component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9cb04351-294b-48ba-8d1c-2f28cb9ce463">UTCSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the UTC component is specified or left as a wildcard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923306">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The full CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eab3738a-c92a-4602-b1ee-e2547da88308">Year</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The year component of a CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/afac0a08-7bd0-42f1-b5a7-8664f9db8615">YearSpecified</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether or not the year is specified or left as a wildcard.

</td>
</tr>
</table> 


## -remarks



WMI records timestamps in universal time coordinate (UTC) format. UTC is not the format that most developers and IT administrators use. Therefore, a common issue is determining how to translate UTC into something more readable. For more information on how to work with UTC, see <a href="https://msdn.microsoft.com/dd01a732-5c88-4c24-a551-4d5452e712cc">WMI Tasks: Dates and Times</a> and <a href="https://TechNet.Microsoft.Com/library/ee198928.aspx">Working with Dates and Times using WMI </a>. You can also read the <a href="https://TechNet.Microsoft.Com/en-us/magazine/2006.07.scriptingguy.aspx">It’s About Time (Oh, and About Dates, Too)</a> and <a href="http://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx">How Can I Subtract a Specified Number of Days from a UTC Value?</a> blog posts for additional information.

Any numeric field can have a wildcard value if the 
    <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> property is set to 
    <b>FALSE</b>. Fields with wildcard values contain asterisks in the entire field.

Each property, for example <a href="https://msdn.microsoft.com/60da99bc-560c-45bc-b787-f4bef8e5a509">Day</a>, has a 
    corresponding specified Boolean value, such as 
    <a href="https://msdn.microsoft.com/a713378b-3953-49d8-9c6a-44aa9337eae2">DaySpecified</a>. When 
    <b>DaySpecified</b> is 
    <b>FALSE</b>, then the value is interpreted as an interval rather than a number between 01 
    and 31. If an interval is used anywhere in the CIM <a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">datetime</a> value, 
    then <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> is also set to 
    <b>TRUE</b>. The default is for a CIM datetime 
    value to contain a date rather than one or more intervals.

For example, if 
    <a href="https://msdn.microsoft.com/a713378b-3953-49d8-9c6a-44aa9337eae2">SWbemDateTime.DaySpecified</a> is 
    <b>TRUE</b>, then 
    <a href="https://msdn.microsoft.com/426a60d5-c364-406e-8346-049a13d59c7f">SWbemDateTime.Value</a> includes the current value of 
    <a href="https://msdn.microsoft.com/60da99bc-560c-45bc-b787-f4bef8e5a509">SWbemDateTime.Day</a>, otherwise it is a wildcard value. 
    The <a href="https://msdn.microsoft.com/ba5fcf17-7c26-4960-9da9-e380d90e5f3e">IsInterval</a> property is 
    <b>FALSE</b> in either case.


#### Examples

The following script code example shows how to use an <b>SWbemDateTime</b> 
     object to parse a datetime property value read from the WMI repository, the 
     <b>InstallDate</b> property in 
     <a href="https://msdn.microsoft.com/eb6a8cff-20a0-4211-b46a-3084e9c39246">Win32_OperatingSystem</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " &amp; dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    &amp; dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    &amp; dateTime.GetFileTime 
next
Set datetime = Nothing</pre>
</td>
</tr>
</table></span></div>
The following example shows how to create an 
      <b>SWbemDateTime</b> object, store a date value in the object, 
      display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and 
      property. For more information about the constant <b>wbemCimtypeDatetime</b>, see 
      <a href="https://msdn.microsoft.com/d9929464-742e-4f6c-b631-a6c191167858">WbemCimtypeEnum</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " &amp; dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " &amp; dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " &amp; dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " &amp; NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
</pre>
</td>
</tr>
</table></span></div>
The following script code example shows how to use an 
      <b>SWbemDateTime</b> object to modify an interval value on a 
      property that is read from the WMI repository.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " &amp; datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " &amp; NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_</pre>
</td>
</tr>
</table></span></div>
The following script code example shows how to use an <b>SWbemDate</b> object to read a 
        <b>FILETIME</b> value.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " &amp; "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " &amp; dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " &amp; dateTime.GetVarDate
Set datetime = Nothing</pre>
</td>
</tr>
</table></span></div>
The following PowerShell code creates an instance of a SWbemDateTime object, 
    retrieves the OS install date, and converts the date to a different format

<div class="code"><span codelanguage="PowerShell"><table>
<tr>
<th>PowerShell</th>
</tr>
<tr>
<td>
<pre># Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
</pre>
</td>
</tr>
</table></span></div>
The following Powershell code translates the code into a format ready to be consumed by a CIM provider.

<div class="code"><span codelanguage="PowerShell"><table>
<tr>
<th>PowerShell</th>
</tr>
<tr>
<td>
<pre> $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2c18ef4d-4eb6-4c73-ad2e-31995b79e99d">DATETIME</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>



<a href="https://msdn.microsoft.com/d9929464-742e-4f6c-b631-a6c191167858">WbemCimtypeEnum</a>
 

 

