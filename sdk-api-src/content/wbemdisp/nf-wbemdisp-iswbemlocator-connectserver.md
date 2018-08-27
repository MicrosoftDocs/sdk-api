---
UID: NF:wbemdisp.ISWbemLocator.ConnectServer
title: ISWbemLocator::ConnectServer
author: windows-sdk-content
description: Connects to the namespace on the computer that is specified in the strServer parameter.
old-location: wmi\swbemlocator_connectserver.htm
old-project: WmiSdk
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ConnectServer, ConnectServer method [Windows Management Instrumentation], ConnectServer method [Windows Management Instrumentation],ISWbemLocator interface, ConnectServer method [Windows Management Instrumentation],SWbemLocator object, ISWbemLocator interface [Windows Management Instrumentation],ConnectServer method, ISWbemLocator.ConnectServer, ISWbemLocator::ConnectServer, SWbemLocator object [Windows Management Instrumentation],ConnectServer method, SWbemLocator.ConnectServer, _hmm_swbemlocator.connectserver, wbemConnectFlagUseMaxWait, wmi.swbemlocator_connectserver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemLocator.ConnectServer
 - ISWbemLocator.ConnectServer
 - ISWbemLocator.ConnectServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemLocator::ConnectServer


## -description


The 
<b>ConnectServer</b> method of the 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a> object connects to the namespace on the computer that is specified in the <i>strServer</i> parameter. The target computer can be either local or remote, but it must have WMI installed. For  examples and a comparison with the moniker type of connection, see <a href="https://msdn.microsoft.com/90e71e17-c2e7-42ad-a72e-2b475e6163fe">Creating a WMI Script</a>.

Starting with Windows Vista, <b>SWbemLocator.ConnectServer</b> can connect with computers running IPv6 using an IPv6 address in the <i>strServer</i> parameter. For more information, see <a href="https://msdn.microsoft.com/8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8">IPv6 and IPv4 Support in WMI</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strServer [in, optional]

Computer name to which you are connecting. If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.  If you do not provide this parameter, the call defaults to the local computer.

Example: <code>server1.network.fabrikam</code>

You also can use an IP address in this parameter. If the IP address is in IPv6 format, the target computer must be running IPv6. An address in IPv4 looks like <code>111.222.333.444</code>

An IP address in IPv6 format looks like  <code>2010:836B:4179::836B:4179</code>

For more information on DNS and IPv4, see the Remarks section.


### -param strNamespace [in, optional]

String that specifies the namespace to which you log on. For example, to log on to the root\default namespace, use root\default. If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting. For more information, see 
<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>.

Example: "root\CIMV2"


### -param strUser [in, optional]

User name to use to connect. The string can be in the form of either a user name or a Domain\Username. Leave this parameter blank to use the current security context. The <i>strUser</i> parameter should only be used with connections to remote WMI servers. If you attempt to specify <i>strUser</i> for a local WMI connection, the connection attempt fails. 


If Kerberos authentication is in use, then the username and password that is specified in <i>strUser</i> and <i>strPassword</i> cannot be intercepted on a network. You can use the UPN format  to specify the <i>strUser</i>.

Example: "DomainName\UserName"

<div class="alert"><b>Note</b>  If a domain is specified in <i>strAuthority</i>, then the domain must not be specified here. Specifying the domain in both parameters results in an Invalid Parameter error.</div>
<div> </div>

### -param strPassword [in, optional]

String that specifies the password to use when attempting to connect. Leave the parameter blank to use the current security context. The <i>strPassword</i> parameter should only be used with connections to remote WMI servers. If you attempt to specify <i>strPassword</i> for a local WMI connection, the connection attempt fails. If Kerberos authentication is in use then the username and password that is specified in <i>strUser</i> and <i>strPassword</i>  cannot be intercepted on the network.


### -param strLocale [in, optional]

String that specifies the localization code. If you want to use the current locale, leave it blank. If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved. For Microsoft locale identifiers, the format of the string is "MS_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID. For example, American English would appear as "MS_409".


### -param strAuthority [in, optional]



#### ""

This parameter is optional. However, if it is specified, only Kerberos or NTLMDomain can be used.



#### Kerberos:

If the <i>strAuthority</i> parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name. The Kerberos principal name is specified as Kerberos:<i>domain</i>, such as <code>Kerberos:fabrikam</code> where <code>fabrikam</code> is the server to which you are attempting to connect.

Example: "Kerberos:DOMAIN"



#### NTLMDomain:

To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:<i>domain</i>, such as <code>NTLMDomain:fabrikam</code> where <code>fabrikam</code> is the name of the domain.

Example: "NTLMDomain:DOMAIN"

If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used. This parameter should only be used with connections to remote WMI servers. If you attempt to set the authority for a local WMI connection, the connection attempt fails.

<div class="alert"><b>Note</b>  If the domain is specified in <i>strUser</i>, which is the preferred location, then it must not be specified here. Specifying the domain in both parameters results in an Invalid Parameter error.</div>
<div> </div>

### -param iSecurityFlags [in, optional]

Used to pass flag values to 
<b>ConnectServer</b>.



#### 0 (0x0)

A value of 0 for this parameter causes the call to 
<b>ConnectServer</b> to return only after the connection to the server is established. This could cause your program to stop responding indefinitely if the connection cannot be established.



#### wbemConnectFlagUseMaxWait (128 (0x80))

The 
<b>ConnectServer</b> call is guaranteed to return in 2 minutes or less. Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.


### -param objWbemNamedValueSet




### -param objWbemServices






#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If successful, WMI returns an <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object that is bound to the namespace that is specified in <i>strNamespace</i> on the computer that is specified in <i>strServer</i>.




## -remarks



The <b>ConnectServer</b> method is often used when connecting to an account with a different username and password—credentials—on a remote computer because you cannot specify a different password in a <a href="https://msdn.microsoft.com/1aacc523-2a2f-43f5-96a3-aa0387cbae3e">moniker</a> string. For more information, see <a href="https://msdn.microsoft.com/16b00ee3-f721-4912-9e8e-2fdbc897a813">Connecting to WMI on a Remote Computer</a>.

Using an IPv4 address to connect to a remote server may result in unexpected behavior. The likely cause is stale DNS entries in your environment. In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results. To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer. This causes the reverse DNS lookup to fail, but may allow the <b>ConnectServer</b> call to succeed on the correct machine.


#### Examples

The following VBScript code example describes how to connect  to a remote computer to obtain <a href="https://msdn.microsoft.com/cb313097-d5d1-4b8e-bee5-20a894c6788d">Win32_IP4RouteTable</a> data. The domain name that is specified in <i>strDomain</i> is used in  <i>strAuthority</i>.


```vb
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```


The following PowerShell snippet access a remote server and lists the available WMI classes.


```powershell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses

```





## -see-also




<a href="https://msdn.microsoft.com/16b00ee3-f721-4912-9e8e-2fdbc897a813">Connecting to WMI on a Remote Computer</a>



<a href="https://msdn.microsoft.com/90e71e17-c2e7-42ad-a72e-2b475e6163fe">Creating a WMI Script</a>



<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

