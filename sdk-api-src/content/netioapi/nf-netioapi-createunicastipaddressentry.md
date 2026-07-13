---
UID: NF:netioapi.CreateUnicastIpAddressEntry
title: CreateUnicastIpAddressEntry function (netioapi.h)
description: Adds a new unicast IP address entry on the local computer.
helpviewer_keywords: ["CreateUnicastIpAddressEntry","CreateUnicastIpAddressEntry function [IP Helper]","iphlp.createunicastipaddressentry","netioapi/CreateUnicastIpAddressEntry"]
old-location: iphlp\createunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: 8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0
ms.date: 12/05/2018
ms.keywords: CreateUnicastIpAddressEntry, CreateUnicastIpAddressEntry function [IP Helper], iphlp.createunicastipaddressentry, netioapi/CreateUnicastIpAddressEntry
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateUnicastIpAddressEntry
 - netioapi/CreateUnicastIpAddressEntry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - CreateUnicastIpAddressEntry
---

# CreateUnicastIpAddressEntry function


## -description

The 
<b>CreateUnicastIpAddressEntry</b> function  adds a new unicast IP address entry on the local computer.

## -parameters

### -param Row [in]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry for a unicast IP address entry.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter was not set to a valid unicast IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> and <b>InterfaceIndex</b> members of the <b>MIB_UNICASTIPADDRESS_ROW</b> pointed to by the <i>Row</i> parameter were unspecified. 

This error is also returned for other errors in the values set for members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure. These errors include the following: if the <b>ValidLifetime</b> member is less than the <b>PreferredLifetime</b> member, if the <b>PrefixOrigin</b> member is set to <b>IpPrefixOriginUnchanged</b> and the <b>SuffixOrigin</b> is the not set to <b>IpSuffixOriginUnchanged</b>, if the <b>PrefixOrigin</b> member is not set to <b>IpPrefixOriginUnchanged</b> and the <b>SuffixOrigin</b> is set to <b>IpSuffixOriginUnchanged</b>, if the <b>PrefixOrigin</b> member is not set to a value from the <b>NL_PREFIX_ORIGIN</b> enumeration, if the <b>SuffixOrigin</b> member is not set to a value from the <b>NL_SUFFIX_ORIGIN</b> enumeration, or if the <b>OnLinkPrefixLength</b> member is set to a value greater than the IP address length, in bits (32 for a unicast IPv4 address or 128 for a unicast IPv6 address).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <b>Address</b> member of the  <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter.  This error is also returned if no IPv6 stack is on the local computer and an IPv6 address was specified in the <b>Address</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_ALREADY_EXISTS </b></dt>
</dl>
</td>
<td width="60%">
The object already exists. This error is returned if the  <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is a duplicate of an existing unicast IP address on the interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <b>MIB_UNICASTIPADDRESS_ROW</b>.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>CreateUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>CreateUnicastIpAddressEntry</b> function is used to add a new unicast IP address entry on a local computer. The unicast IP address added by 
the <b>CreateUnicastIpAddressEntry</b> function is not persistent. The IP address exists only as long as the adapter object exists. Restarting the computer destroys the IP address, as does manually resetting the network interface card (NIC). Also, certain PnP events may destroy the address.

To create an IPv4 address that persists, the <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration">EnableStatic method of the Win32_NetworkAdapterConfiguration Class</a> in the Windows Management Instrumentation (WMI) controls may be used. The netsh command can also be used to create a persistent IPv4 or IPv6 address. 

For more information, please see the documentation on <a href="/windows/desktop/WinSock/netsh-exe">Netsh.exe</a> in the Windows Sockets documentation.

The <a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a> function should be used to initialize the members of a
    <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry with default values.  An application can then change the
    members in the <b>MIB_UNICASTIPADDRESS_ROW</b> entry it wishes to modify, and then call the <b>CreateUnicastIpAddressEntry</b> function.

The <b>Address</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid unicast IPv4 or IPv6 address. The <b>si_family</b> member of the <b>SOCKADDR_INET</b> structure  in the  <b>Address</b> member must be initialized to either <b>AF_INET</b> or <b>AF_INET6</b> and the related <b>Ipv4</b> or <b>Ipv6</b> member of the  <b>SOCKADDR_INET</b> structure must be set to a valid unicast IP address. In addition, at least one of the following members in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized to the interface: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface on which to add the unicast IP address. If no value was set for the  <b>InterfaceLuid</b> member (the values of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

If the <b>OnLinkPrefixLength</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is set to 255, then <b>CreateUnicastIpAddressEntry</b> will add the new unicast IP address with the  <b>OnLinkPrefixLength</b> member set equal to the length of the IP address. So for a unicast IPv4 address, the  <b>OnLinkPrefixLength</b> is set to 32 and the <b>OnLinkPrefixLength</b> is set to 128 for a unicast IPv6 address. If this would result in the incorrect subnet mask for an IPv4 address or the incorrect link prefix for an IPv6 address, then the application should set this member to the correct value before calling <b>CreateUnicastIpAddressEntry</b>. 

If a unicast IP address is created with the <b>OnLinkPrefixLength</b> member set incorrectly, then the IP address may be changed by calling <a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a> with the  <b>OnLinkPrefixLength</b> member set to the correct value.

The <b>DadState</b>, <b>ScopeId</b>, and <b>CreationTimeStamp</b> members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> are ignored when the  <b>CreateUnicastIpAddressEntry</b> function is called. These members are set by the network stack. The  <b>ScopeId</b> member is automatically determined by the interface on which the address is added. Beginning in Windows 10, if <b>DadState</b> is set to <b>IpDadStatePreferred</b> in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure when calling <b>CreateUnicastIpAddressEntry</b>, the stack will set the initial DAD state of the address to “preferred” instead of “tentative” and will do optimistic DAD for the address.

The <b>CreateUnicastIpAddressEntry</b> function will fail if the unicast IP address passed in the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is a duplicate of an existing unicast IP address on the interface. Note that a loopback IP address can only be added to a loopback interface using the <b>CreateUnicastIpAddressEntry</b> function. 

The unicast IP address passed in the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is not usable immediately. The IP address is usable after the duplicate address detection process has completed successfully. It can take several seconds for the duplicate address detection process to complete since IP packets need to  be sent and potential responses must be awaited. For IPv6, the duplicate address detection process typically takes about a second. For IPv4, the duplicate address detection process typically takes about three seconds. 

If an application that needs to know when an IP address is usable after a call to  the <b>CreateUnicastIpAddressEntry</b> function, there are two methods that can be used. One method uses polling and the <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> function. The second method calls one of the notification functions, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a>, <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>, or <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a> to set up an asynchronous notification for when an address changes.

The following method describes how to use the <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> and polling. After the call to the <b>CreateUnicastIpAddressEntry</b> function returns successfully, pause for one to three seconds (depending on whether an IPv6 or IPv4 address is being created) to allow time for the successful completion of the duplication address detection process. Then call the <b>GetUnicastIpAddressEntry</b> function to retrieve the updated <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure and examine the value of the <b>DadState</b> member. If the value of the <b>DadState</b> member is set to <b>IpDadStatePreferred</b>, the IP address is now usable.  If the value of the <b>DadState</b> member is set to <b>IpDadStateTentative</b>, then duplicate address detection has not yet completed. In this case, call the <b>GetUnicastIpAddressEntry</b> function again every half a second while the <b>DadState</b> member is still set to <b>IpDadStateTentative</b>. If the value of the <b>DadState</b> member returns with some value other than <b>IpDadStatePreferred</b> or <b>IpDadStateTentative</b>, duplicate address detection has failed and the IP address is not usable.  

The following method describes how to use an appropriate notification function. After the call to the <b>CreateUnicastIpAddressEntry</b> function returns successfully, call the <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a> function to register to be notified of changes to either IPv6 or IPv4 unicast IP addresses, depending on the type of IP address being created. When a notification is received for the IP address being created, call the <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> function to retrieve the <b>DadState</b> member.  If the value of the <b>DadState</b> member is set to <b>IpDadStatePreferred</b>, the IP address is now usable.  If the value of the <b>DadState</b> member is set to <b>IpDadStateTentative</b>, then duplicate address detection has not yet completed and the application needs to wait for future notifications. If the value of the <b>DadState</b> member returns with some value other than <b>IpDadStatePreferred</b> or <b>IpDadStateTentative</b>, duplicate address detection has failed and the IP address is not usable.  

If during the duplicate address detection process the media is disconnected and then reconnected, the duplicate address detection process is restarted. So it is possible for the time to complete the process to increase beyond the typical 1 second value for IPv6 or 3 second value for IPv4.

The <b>CreateUnicastIpAddressEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateUnicastIpAddressEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and ERROR_ACCESS_DENIED is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.




#### Examples

The following example demonstrates how to use the <b>CreateUnicastIpAddressEntry</b> function to add a new unicast IP address entry on the local computer. 


```cpp

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2ipdef.h> 
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Iphlpapi.lib and Ws2_32.lib
#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

HANDLE gCallbackComplete;
HANDLE gNotifyEvent;

void CALLBACK CallCompleted (VOID *callerContext, 
    PMIB_UNICASTIPADDRESS_ROW row, 
    MIB_NOTIFICATION_TYPE notificationType);

int main(int argc, char **argv)  {

    // Declare and initialize variables
    
    unsigned long ipAddress = INADDR_NONE;
    unsigned long ipMask = INADDR_NONE;

    DWORD dwRetVal = 0;

    DWORD dwSize = 0;
    unsigned long status = 0;

    DWORD lastError = 0;
    SOCKADDR_IN localAddress;

    NET_LUID interfaceLuid;
    PMIB_IPINTERFACE_TABLE pipTable = NULL; 
    MIB_UNICASTIPADDRESS_ROW ipRow;

    // Validate the parameters
    if (argc != 3) {
        printf("usage: %s IPv4address IPv4mask\n", argv[0]);
        exit(1);
    }

    ipAddress = inet_addr(argv[1]);
    if (ipAddress == INADDR_NONE) {
        printf("usage: %s IPv4address IPv4mask\n", argv[0]);
        exit(1);
    }

    ipMask = inet_addr(argv[2]);
    if (ipMask == INADDR_NONE) {
        printf("usage: %s IPv4address IPv4mask\n", argv[0]);
        exit(1);
    }


    status = GetIpInterfaceTable( AF_INET, &pipTable );
    if( status != NO_ERROR )
    {
        printf("GetIpInterfaceTable returned error: %ld\n", 
            status);
        exit(1);
    }

    // Use loopback interface
    interfaceLuid = pipTable->Table[0].InterfaceLuid;

    localAddress.sin_family            = AF_INET;
    localAddress.sin_addr.S_un.S_addr  = ipAddress;
    
    FreeMibTable(pipTable);
    pipTable = NULL;    

    // Initialize the row
    InitializeUnicastIpAddressEntry( &ipRow );

    ipRow.InterfaceLuid = interfaceLuid;
    ipRow.Address.Ipv4 = localAddress;

    // Create a Handle to be notified of IP address changes
    gCallbackComplete = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (gCallbackComplete == NULL) {
        printf("CreateEvent failed with error: %d\n", GetLastError() );
        exit(1);
    }    
    
    // Use NotifyUnicastIpAddressChange to determine when the address is ready
    NotifyUnicastIpAddressChange(AF_INET, &CallCompleted, NULL, FALSE, &gNotifyEvent);

    status = CreateUnicastIpAddressEntry(&ipRow);
    if(status != NO_ERROR)
    {
        CancelMibChangeNotify2(gNotifyEvent);
        switch(status)
        {
            case ERROR_INVALID_PARAMETER:
                printf("Error: CreateUnicastIpAddressEntry returned ERROR_INVALID_PARAMETER\n");
                break;
            case ERROR_NOT_FOUND:
                printf("Error: CreateUnicastIpAddressEntry returned ERROR_NOT_FOUND\n");
                break;
            case ERROR_NOT_SUPPORTED:
                printf("Error: CreateUnicastIpAddressEntry returned ERROR_NOT_SUPPORTED\n");
                break;
            case ERROR_OBJECT_ALREADY_EXISTS:
                printf("Error: CreateUnicastIpAddressEntry returned ERROR_OBJECT_ALREADY_EXISTS\n");
                break;
            default:
                //NOTE: Is this case needed? If not, we can remove the ErrorExit() function
                printf("CreateUnicastIpAddressEntry returned error: %d\n", status);
                break;
        }
        exit (status);
        
    }
    else
        printf("CreateUnicastIpAddressEntry succeeded\n");
        
    // Set timeout to 6 seconds
    status = WaitForSingleObject(gCallbackComplete, 6000);
    if(status != WAIT_OBJECT_0)
    {
        CancelMibChangeNotify2(gNotifyEvent);
        CancelMibChangeNotify2(gCallbackComplete);
        switch(status)
        {
            case WAIT_ABANDONED:
                printf("Wait on event was abandoned\n");
                break;
            case WAIT_TIMEOUT:
                printf("Wait on event timed out\n");
                break;
            default:
                printf("Wait on event exited with status %d\n", status);
                break;
        }
        return status;
    }
    printf("Task completed successfully\n");
    CancelMibChangeNotify2(gNotifyEvent);
    CancelMibChangeNotify2(gCallbackComplete);

    exit (0);
}


void CALLBACK CallCompleted(PVOID callerContext, PMIB_UNICASTIPADDRESS_ROW row, MIB_NOTIFICATION_TYPE notificationType)
{

    ADDRESS_FAMILY addressFamily; 
    SOCKADDR_IN sockv4addr;
    struct in_addr ipv4addr;
    
    // Ensure that this is the correct notification before setting gCallbackComplete
    // NOTE: Is there a stronger way to do this?
    if(notificationType == MibAddInstance) {
        printf("NotifyUnicastIpAddressChange received an Add instance\n");
        addressFamily = (ADDRESS_FAMILY) row->Address.si_family;
        switch (addressFamily) {
            case AF_INET:
                printf("\tAddressFamily: AF_INET\n");
                break;
            case AF_INET6:
                printf("\tAddressFamily: AF_INET6\n");
                break;
            default:    
                printf("\tAddressFamily: %d\n", addressFamily);
                break;
       }
       if (addressFamily == AF_INET) {
            sockv4addr = row->Address.Ipv4;
            ipv4addr = sockv4addr.sin_addr;
            printf("IPv4 address:  %s\n", inet_ntoa(ipv4addr) );
       }     
       if (callerContext != NULL)
           printf("Received a CallerContext value\n");
           
       SetEvent(gCallbackComplete);
    }    
    return;
}

```

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteunicastipaddressentry">DeleteUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/WinSock/netsh-exe">Netsh.exe</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>