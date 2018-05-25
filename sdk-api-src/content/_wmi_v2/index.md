---
UID: TP:wmi_v2
ms.assetid: 824b23dd-9cc9-3dd8-bc5a-af4068a53abd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Windows Management Infrastructure (MI)



Overview of the Windows Management Infrastructure (MI) technology.

To develop Windows Management Infrastructure (MI), you need these headers:

 * [mi.h](..\mi\index.md)

For the programming guide, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2).

## Functions

| Title   | Description   |
| ---- |:---- |
| [MI_Application_Close function](..\mi\nf-mi-mi_application_close.md) | Deinitializes the management infrastructure client API that was initialized through a call to MI_Application_Initialize. |
| [MI_Application_InitializeV1 function](..\mi\nf-mi-mi_application_initializev1.md) | Initializes an application so that it can make Management Infrastructure (MI) client API calls. |
| [MI_Application_NewClass function](..\mi\nf-mi-mi_application_newclass.md) | Creates an MI_Class from an MI_ClassDecl structure. |
| [MI_Application_NewDeserializer function](..\mi\nf-mi-mi_application_newdeserializer.md) | Creates a deserializer object that can then be used to convert a serialized object back into a class or instance. |
| [MI_Application_NewDestinationOptions function](..\mi\nf-mi-mi_application_newdestinationoptions.md) | Creates an MI_DestinationOptions object that can be used with the MI_Application_NewSession function. |
| [MI_Application_NewHostedProvider function](..\mi\nf-mi-mi_application_newhostedprovider.md) | Registers a hosted provider with the WMI engine on the local machine. |
| [MI_Application_NewInstance function](..\mi\nf-mi-mi_application_newinstance.md) | Creates a new MI_Instance object to be passed to various MI operation APIs that require instances. |
| [MI_Application_NewInstanceFromClass function](..\mi\nf-mi-mi_application_newinstancefromclass.md) | Creates a new MI_Instance object based on a class object. |
| [MI_Application_NewOperationOptions function](..\mi\nf-mi-mi_application_newoperationoptions.md) | Creates an MI_OperationOptions object that can be used with the operation functions on the MI_Session object. |
| [MI_Application_NewParameterSet function](..\mi\nf-mi-mi_application_newparameterset.md) | Creates a new parameter set. |
| [MI_Application_NewSerializer function](..\mi\nf-mi-mi_application_newserializer.md) | Retrieves a serializer object that can then be used to serialize instances and classes into various different formats. |
| [MI_Application_NewSession function](..\mi\nf-mi-mi_application_newsession.md) | Creates a session used to share connections for a set of operations to a single destination. |
| [MI_Application_NewSubscriptionDeliveryOptions function](..\mi\nf-mi-mi_application_newsubscriptiondeliveryoptions.md) | Creates an MI_SubscriptionDeliveryOptions object that represents the configuration needed to carry out subscribe operations over certain protocols. |
| [MI_Class_Clone function](..\mi\nf-mi-mi_class_clone.md) | Clones an MI_Class object. |
| [MI_Class_Delete function](..\mi\nf-mi-mi_class_delete.md) | Deletes an MI_Class object. |
| [MI_Class_GetClassName function](..\mi\nf-mi-mi_class_getclassname.md) | Gets the class name of the specified class. |
| [MI_Class_GetClassQualifierSet function](..\mi\nf-mi-mi_class_getclassqualifierset.md) | Gets the qualifier set that is associated with the specified class object. |
| [MI_Class_GetElement function](..\mi\nf-mi-mi_class_getelement.md) | Gets all details of a specified named element from a class. |
| [MI_Class_GetElementAt function](..\mi\nf-mi-mi_class_getelementat.md) | Gets details of a class element based on the element index. |
| [MI_Class_GetElementCount function](..\mi\nf-mi-mi_class_getelementcount.md) | Gets the number of elements in a class. |
| [MI_Class_GetMethod function](..\mi\nf-mi-mi_class_getmethod.md) | Gets details of a method based on the method name. |
| [MI_Class_GetMethodAt function](..\mi\nf-mi-mi_class_getmethodat.md) | Gets details of a method based on the method index. |
| [MI_Class_GetMethodCount function](..\mi\nf-mi-mi_class_getmethodcount.md) | Gets the number of methods in the class. |
| [MI_Class_GetNameSpace function](..\mi\nf-mi-mi_class_getnamespace.md) | Gets the namespace name of the specified class. |
| [MI_Class_GetParentClass function](..\mi\nf-mi-mi_class_getparentclass.md) | Gets the parent class for the specified class. |
| [MI_Class_GetParentClassName function](..\mi\nf-mi-mi_class_getparentclassname.md) | Gets the parent class name of the specified class. |
| [MI_Class_GetServerName function](..\mi\nf-mi-mi_class_getservername.md) | Gets the name of the server from the specified class. |
| [MI_Context_Canceled function](..\mi\nf-mi-mi_context_canceled.md) | Determines whether the operation has been canceled. This function is reserved; instead, use the MI_Context_RegisterCancel function. |
| [MI_Context_ConstructInstance function](..\mi\nf-mi-mi_context_constructinstance.md) | Initializes an MI class instance on the stack or as a member of a structure. |
| [MI_Context_ConstructParameters function](..\mi\nf-mi-mi_context_constructparameters.md) | A provider calls this function to initialize a parameter's instance. |
| [MI_Context_GetCustomOption function](..\mi\nf-mi-mi_context_getcustomoption.md) | Retrieves an option set by the client. |
| [MI_Context_GetCustomOptionAt function](..\mi\nf-mi-mi_context_getcustomoptionat.md) | Retrieves an option at a particular index that was set by the client. |
| [MI_Context_GetCustomOptionCount function](..\mi\nf-mi-mi_context_getcustomoptioncount.md) | Gets the number of custom options available to the provider. |
| [MI_Context_GetLocalSession function](..\mi\nf-mi-mi_context_getlocalsession.md) | Gets the local session (MI_Session) which allows the provider to perform CIM operations against the local server hosting the provider. |
| [MI_Context_GetLocale function](..\mi\nf-mi-mi_context_getlocale.md) | Retrieves the requested locale information that the client specified for the operation. |
| [MI_Context_GetNumberOption function](..\mi\nf-mi-mi_context_getnumberoption.md) | Gets the numeric option that the client sets, based on the operation name. |
| [MI_Context_GetStringOption function](..\mi\nf-mi-mi_context_getstringoption.md) | Gets the string option that the client sets, based on the operation name. |
| [MI_Context_NewDynamicInstance function](..\mi\nf-mi-mi_context_newdynamicinstance.md) | Creates a new dynamic instance (weakly typed instance without a class declaration) of a class. |
| [MI_Context_NewInstance function](..\mi\nf-mi-mi_context_newinstance.md) | Creates a new instance of a class given a class declaration. |
| [MI_Context_NewParameters function](..\mi\nf-mi-mi_context_newparameters.md) | Creates a new instance of a method given a method declaration. |
| [MI_Context_PostCimError function](..\mi\nf-mi-mi_context_postcimerror.md) | Posts a return code and an error message (in the form of a CIM_Error object) to the server in response to a request. |
| [MI_Context_PostError function](..\mi\nf-mi-mi_context_posterror.md) | Providers call this function to post a return code to the client in response to a request. |
| [MI_Context_PostIndication function](..\mi\nf-mi-mi_context_postindication.md) | Posts an indication result to the server in response to a subscribe operation request. |
| [MI_Context_PostInstance function](..\mi\nf-mi-mi_context_postinstance.md) | Posts an instance back to the client (through the server) in response to a request. |
| [MI_Context_PostResult function](..\mi\nf-mi-mi_context_postresult.md) | Posts the final terminating result code back to the client (through the server) in response to a request. |
| [MI_Context_PromptUser function](..\mi\nf-mi-mi_context_promptuser.md) | Sends a prompt message to the client querying whether to continue the operation or cancel it. |
| [MI_Context_RefuseUnload function](..\mi\nf-mi-mi_context_refuseunload.md) | Tells the provider infrastructure not to unload the provider. |
| [MI_Context_RegisterCancel function](..\mi\nf-mi-mi_context_registercancel.md) | Registers a callback that is invoked when the operation is canceled. |
| [MI_Context_RequestUnload function](..\mi\nf-mi-mi_context_requestunload.md) | Requests to unload the module or the provider. |
| [MI_Context_SetStringOption function](..\mi\nf-mi-mi_context_setstringoption.md) | Sets a context-specific option. |
| [MI_Context_ShouldContinue function](..\mi\nf-mi-mi_context_shouldcontinue.md) | Queries the client to determine if an operation should continue. |
| [MI_Context_ShouldProcess function](..\mi\nf-mi-mi_context_shouldprocess.md) | Queries the client to determine if an operation should continue. |
| [MI_Context_WriteCimError function](..\mi\nf-mi-mi_context_writecimerror.md) | Sends a CIM (informative) error instance to the client. |
| [MI_Context_WriteDebug function](..\mi\nf-mi-mi_context_writedebug.md) | Sends a debug message to the client. |
| [MI_Context_WriteError function](..\mi\nf-mi-mi_context_writeerror.md) | Sends an error code and error message to the client. |
| [MI_Context_WriteMessage function](..\mi\nf-mi-mi_context_writemessage.md) | Sends an operational message to the client. |
| [MI_Context_WriteProgress function](..\mi\nf-mi-mi_context_writeprogress.md) | Sends a progress message to the client. |
| [MI_Context_WriteStreamParameter function](..\mi\nf-mi-mi_context_writestreamparameter.md) | Sends streamed parameter data to the client for a method invocation. |
| [MI_Context_WriteVerbose function](..\mi\nf-mi-mi_context_writeverbose.md) | Writes a verbose message to the client. |
| [MI_Context_WriteWarning function](..\mi\nf-mi-mi_context_writewarning.md) | Writes a warning message to the client. |
| [MI_Deserializer_Class_GetClassName function](..\mi\nf-mi-mi_deserializer_class_getclassname.md) | Gets the class name from a serialized class buffer. |
| [MI_Deserializer_Class_GetParentClassName function](..\mi\nf-mi-mi_deserializer_class_getparentclassname.md) | Gets the parent class name from a serialized class buffer. |
| [MI_Deserializer_Close function](..\mi\nf-mi-mi_deserializer_close.md) | Closes a deserializer object and deletes any associated memory that is held within the deserializer. |
| [MI_Deserializer_DeserializeClass function](..\mi\nf-mi-mi_deserializer_deserializeclass.md) | Deserializes a serialized buffer into an MI_Class object. |
| [MI_Deserializer_DeserializeInstance function](..\mi\nf-mi-mi_deserializer_deserializeinstance.md) | Deserializes a serialized buffer into a MI_Instance object. |
| [MI_Deserializer_Instance_GetClassName function](..\mi\nf-mi-mi_deserializer_instance_getclassname.md) | Gets the class name associated with the serialized instance. |
| [MI_DestinationOptions_AddDestinationCredentials function](..\mi\nf-mi-mi_destinationoptions_adddestinationcredentials.md) | Sets the credentials for talking to the destination. |
| [MI_DestinationOptions_AddProxyCredentials function](..\mi\nf-mi-mi_destinationoptions_addproxycredentials.md) | Adds credentials to authenticate against a proxy. |
| [MI_DestinationOptions_Clone function](..\mi\nf-mi-mi_destinationoptions_clone.md) | Creates a copy of a MI_DestinationOptions structure. |
| [MI_DestinationOptions_Delete function](..\mi\nf-mi-mi_destinationoptions_delete.md) | Deletes the destination options structure created by using the MI_Application_NewDestinationOptions or MI_DestinationOptions_Clone function. |
| [MI_DestinationOptions_GetCertCACheck function](..\mi\nf-mi-mi_destinationoptions_getcertcacheck.md) | Gets the server certificate CA check value. |
| [MI_DestinationOptions_GetCertCNCheck function](..\mi\nf-mi-mi_destinationoptions_getcertcncheck.md) | Gets the server certificate CN check value. |
| [MI_DestinationOptions_GetCertRevocationCheck function](..\mi\nf-mi-mi_destinationoptions_getcertrevocationcheck.md) | Gets the server certificate's revocation check value. |
| [MI_DestinationOptions_GetCredentialsAt function](..\mi\nf-mi-mi_destinationoptions_getcredentialsat.md) | Get the credentials at the specified index. |
| [MI_DestinationOptions_GetCredentialsCount function](..\mi\nf-mi-mi_destinationoptions_getcredentialscount.md) | Gets the number of previously added credentials. |
| [MI_DestinationOptions_GetCredentialsPasswordAt function](..\mi\nf-mi-mi_destinationoptions_getcredentialspasswordat.md) | Gets a credentials password based on a specified index. |
| [MI_DestinationOptions_GetDataLocale function](..\mi\nf-mi-mi_destinationoptions_getdatalocale.md) | Gets the data locale (as opposed to UI locale) set by the user. |
| [MI_DestinationOptions_GetDestinationPort function](..\mi\nf-mi-mi_destinationoptions_getdestinationport.md) | Gets the default port for transport. |
| [MI_DestinationOptions_GetEncodePortInSPN function](..\mi\nf-mi-mi_destinationoptions_getencodeportinspn.md) | Gets the port's Service Principal Name encoding value. |
| [MI_DestinationOptions_GetHttpUrlPrefix function](..\mi\nf-mi-mi_destinationoptions_gethttpurlprefix.md) | Gets the HTTP URL prefix. |
| [MI_DestinationOptions_GetImpersonationType function](..\mi\nf-mi-mi_destinationoptions_getimpersonationtype.md) | Gets the impersonation type. |
| [MI_DestinationOptions_GetMaxEnvelopeSize function](..\mi\nf-mi-mi_destinationoptions_getmaxenvelopesize.md) | Gets the maximum size of the packet sent to a server or received by the client from the server. |
| [MI_DestinationOptions_GetNumber function](..\mi\nf-mi-mi_destinationoptions_getnumber.md) | Gets a previously added custom number option. |
| [MI_DestinationOptions_GetOption function](..\mi\nf-mi-mi_destinationoptions_getoption.md) | Gets a previously added option value based on the option name. |
| [MI_DestinationOptions_GetOptionAt function](..\mi\nf-mi-mi_destinationoptions_getoptionat.md) | Gets a previously added option value based on the specified index. |
| [MI_DestinationOptions_GetOptionCount function](..\mi\nf-mi-mi_destinationoptions_getoptioncount.md) | Gets the number of options previously added. |
| [MI_DestinationOptions_GetPacketEncoding function](..\mi\nf-mi-mi_destinationoptions_getpacketencoding.md) | Gets the previously set packet encoding setting. |
| [MI_DestinationOptions_GetPacketIntegrity function](..\mi\nf-mi-mi_destinationoptions_getpacketintegrity.md) | Gets the packet integrity setting. |
| [MI_DestinationOptions_GetPacketPrivacy function](..\mi\nf-mi-mi_destinationoptions_getpacketprivacy.md) | Gets the packet privacy (encryption) setting. |
| [MI_DestinationOptions_GetProxyType function](..\mi\nf-mi-mi_destinationoptions_getproxytype.md) | Gets the proxy type set by the user. |
| [MI_DestinationOptions_GetString function](..\mi\nf-mi-mi_destinationoptions_getstring.md) | Gets a previously added custom string option. |
| [MI_DestinationOptions_GetTimeout function](..\mi\nf-mi-mi_destinationoptions_gettimeout.md) | Gets the default options timeout value. |
| [MI_DestinationOptions_GetTransport function](..\mi\nf-mi-mi_destinationoptions_gettransport.md) | Gets the transport setting that the client added. |
| [MI_DestinationOptions_GetUILocale function](..\mi\nf-mi-mi_destinationoptions_getuilocale.md) | Gets the user interface locale set by the user. |
| [MI_DestinationOptions_SetCertCACheck function](..\mi\nf-mi-mi_destinationoptions_setcertcacheck.md) | Enables or disables the CA certificate check for an SSL transport. |
| [MI_DestinationOptions_SetCertCNCheck function](..\mi\nf-mi-mi_destinationoptions_setcertcncheck.md) | Enables or disables the certificate CN check when an SSL transport is used. |
| [MI_DestinationOptions_SetCertRevocationCheck function](..\mi\nf-mi-mi_destinationoptions_setcertrevocationcheck.md) | Enables or disables the certificate revocation when communicating over SSL. |
| [MI_DestinationOptions_SetDataLocale function](..\mi\nf-mi-mi_destinationoptions_setdatalocale.md) | Sets the default data locale to use for operations. |
| [MI_DestinationOptions_SetDestinationPort function](..\mi\nf-mi-mi_destinationoptions_setdestinationport.md) | Set the port to use to communicate to the destination. |
| [MI_DestinationOptions_SetEncodePortInSPN function](..\mi\nf-mi-mi_destinationoptions_setencodeportinspn.md) | Enables or disables the encoding of the port number in the Service Principal Name when establishing a connection to a remote machine. |
| [MI_DestinationOptions_SetHttpUrlPrefix function](..\mi\nf-mi-mi_destinationoptions_sethttpurlprefix.md) | Set the default HTTP URL prefix for transports that go over HTTP and HTTPS. |
| [MI_DestinationOptions_SetImpersonationType function](..\mi\nf-mi-mi_destinationoptions_setimpersonationtype.md) | Sets the impersonation type. |
| [MI_DestinationOptions_SetMaxEnvelopeSize function](..\mi\nf-mi-mi_destinationoptions_setmaxenvelopesize.md) | Sets the maximum packet size for transports. |
| [MI_DestinationOptions_SetNumber function](..\mi\nf-mi-mi_destinationoptions_setnumber.md) | Sets a custom numeric option value. |
| [MI_DestinationOptions_SetPacketEncoding function](..\mi\nf-mi-mi_destinationoptions_setpacketencoding.md) | Sets the encoding mechanism for certain protocol handles. |
| [MI_DestinationOptions_SetPacketIntegrity function](..\mi\nf-mi-mi_destinationoptions_setpacketintegrity.md) | Enables or disables packet integrity (signing) of a protocol connection. |
| [MI_DestinationOptions_SetPacketPrivacy function](..\mi\nf-mi-mi_destinationoptions_setpacketprivacy.md) | Enables or disables packet privacy (encryption). |
| [MI_DestinationOptions_SetProxyType function](..\mi\nf-mi-mi_destinationoptions_setproxytype.md) | Sets the type of proxy settings to use when communicating to a destination through a proxy. |
| [MI_DestinationOptions_SetString function](..\mi\nf-mi-mi_destinationoptions_setstring.md) | Sets a custom string option. |
| [MI_DestinationOptions_SetTimeout function](..\mi\nf-mi-mi_destinationoptions_settimeout.md) | Sets the default options timeout value. |
| [MI_DestinationOptions_SetTransport function](..\mi\nf-mi-mi_destinationoptions_settransport.md) | Sets the transport to be used to communicate with the destination machine. |
| [MI_DestinationOptions_SetUILocale function](..\mi\nf-mi-mi_destinationoptions_setuilocale.md) | Sets the default UI locale for operations. |
| [MI_Filter_Evaluate function](..\mi\nf-mi-mi_filter_evaluate.md) | The provider calls this function to evaluate an instance against a given filter. |
| [MI_Filter_GetExpression function](..\mi\nf-mi-mi_filter_getexpression.md) | Gets the filter language and expression. |
| [MI_HostedProvider_Close function](..\mi\nf-mi-mi_hostedprovider_close.md) | Close a hosted provider handle that was returned from MI_Application_NewHostedProvider. |
| [MI_HostedProvider_GetApplication function](..\mi\nf-mi-mi_hostedprovider_getapplication.md) | Gets the top-level application handle from which the hosted provider handle was created. |
| [MI_Instance_AddElement function](..\mi\nf-mi-mi_instance_addelement.md) | Adds a new property to a dynamic instance (supported only by dynamic instances whose schema may be extended at run time). |
| [MI_Instance_ClearElement function](..\mi\nf-mi-mi_instance_clearelement.md) | Clears the value of the named element (CIM property) and sets it to NULL. |
| [MI_Instance_ClearElementAt function](..\mi\nf-mi-mi_instance_clearelementat.md) | Clears the value of the element (CIM property) at the specified index and sets it to NULL. |
| [MI_Instance_Clone function](..\mi\nf-mi-mi_instance_clone.md) | Creates a copy of the specified instance on the heap. |
| [MI_Instance_Delete function](..\mi\nf-mi-mi_instance_delete.md) | Deletes an instance that was created on the heap or cloned from another instance. |
| [MI_Instance_Destruct function](..\mi\nf-mi-mi_instance_destruct.md) | Deletes an instance that was created on the stack or as a member of a structure. |
| [MI_Instance_GetClass function](..\mi\nf-mi-mi_instance_getclass.md) | Gets the MI_Class associated with an instance. |
| [MI_Instance_GetClassName function](..\mi\nf-mi-mi_instance_getclassname.md) | Gets the class name of the specified instance. |
| [MI_Instance_GetElement function](..\mi\nf-mi-mi_instance_getelement.md) | Gets the value of the named element (CIM property). |
| [MI_Instance_GetElementAt function](..\mi\nf-mi-mi_instance_getelementat.md) | Gets the value of the element (CIM property) at the specified index. |
| [MI_Instance_GetElementCount function](..\mi\nf-mi-mi_instance_getelementcount.md) | Gets the number of elements in an instance. |
| [MI_Instance_GetNameSpace function](..\mi\nf-mi-mi_instance_getnamespace.md) | Gets the namespace name of the specified instance. |
| [MI_Instance_GetServerName function](..\mi\nf-mi-mi_instance_getservername.md) | Gets the server name from the specified instance. |
| [MI_Instance_IsA function](..\mi\nf-mi-mi_instance_isa.md) | Determines if the instance self is an instance of the class given by classDecl. |
| [MI_Instance_Normalize function](..\mi\nf-mi-mi_instance_normalize.md) | Parses an MI_Instance_ExFT structure and then retrieves the MI_InstanceFT function table. |
| [MI_Instance_SetElement function](..\mi\nf-mi-mi_instance_setelement.md) | Set the value of the element with the given name in the given instance. |
| [MI_Instance_SetElementAt function](..\mi\nf-mi-mi_instance_setelementat.md) | Set the value of the element at the given index of an instance. |
| [MI_Instance_SetNameSpace function](..\mi\nf-mi-mi_instance_setnamespace.md) | Sets the namespace name of the specified instance. |
| [MI_Instance_SetServerName function](..\mi\nf-mi-mi_instance_setservername.md) | Sets the server name of the specified instance. |
| [MI_OperationOptions_Clone function](..\mi\nf-mi-mi_operationoptions_clone.md) | Creates a copy of a MI_OperationOptions structure. |
| [MI_OperationOptions_Delete function](..\mi\nf-mi-mi_operationoptions_delete.md) | Deletes an option set and its associated memory. |
| [MI_OperationOptions_DisableChannel function](..\mi\nf-mi-mi_operationoptions_disablechannel.md) | Uses MI_Context_WriteMessage to disable logging to the specified channel. |
| [MI_OperationOptions_EnableChannel function](..\mi\nf-mi-mi_operationoptions_enablechannel.md) | Uses MI_Context_WriteMessage to enable logging to the specified channel. |
| [MI_OperationOptions_GetEnabledChannels function](..\mi\nf-mi-mi_operationoptions_getenabledchannels.md) | Gets the list of previously enabled channels. |
| [MI_OperationOptions_GetNumber function](..\mi\nf-mi-mi_operationoptions_getnumber.md) | Gets a previously added custom number option. |
| [MI_OperationOptions_GetOption function](..\mi\nf-mi-mi_operationoptions_getoption.md) | Gets a previously added option value based on the option name. |
| [MI_OperationOptions_GetOptionAt function](..\mi\nf-mi-mi_operationoptions_getoptionat.md) | Gets a previously added option value based on the specified index. |
| [MI_OperationOptions_GetOptionCount function](..\mi\nf-mi-mi_operationoptions_getoptioncount.md) | Gets the number of options previously added. |
| [MI_OperationOptions_GetPromptUserMode function](..\mi\nf-mi-mi_operationoptions_getpromptusermode.md) | Gets the value that tells the server how to respond to a provider's call to MI_Context_PromptUser. |
| [MI_OperationOptions_GetPromptUserRegularMode function](..\mi\nf-mi-mi_operationoptions_getpromptuserregularmode.md) | Gets the value that tells the server how to respond to a provider's call to MI_Context_PromptUser. |
| [MI_OperationOptions_GetProviderArchitecture function](..\mi\nf-mi-mi_operationoptions_getproviderarchitecture.md) | Gets the provider architecture for an operation. |
| [MI_OperationOptions_GetResourceUri function](..\mi\nf-mi-mi_operationoptions_getresourceuri.md) | Gets the resource URI being used for an operation. |
| [MI_OperationOptions_GetResourceUriPrefix function](..\mi\nf-mi-mi_operationoptions_getresourceuriprefix.md) | Gets the resource URI prefix being used for an operation. |
| [MI_OperationOptions_GetString function](..\mi\nf-mi-mi_operationoptions_getstring.md) | Gets a custom string option. |
| [MI_OperationOptions_GetTimeout function](..\mi\nf-mi-mi_operationoptions_gettimeout.md) | Gets the operation timeout value. |
| [MI_OperationOptions_GetUseMachineID function](..\mi\nf-mi-mi_operationoptions_getusemachineid.md) | Gets the value that indicates whether to use machine identification information in the operation request. |
| [MI_OperationOptions_GetWriteErrorMode function](..\mi\nf-mi-mi_operationoptions_getwriteerrormode.md) | Sets the error reporting mode. |
| [MI_OperationOptions_SetCustomOption function](..\mi\nf-mi-mi_operationoptions_setcustomoption.md) | Sets a custom option for the operation. |
| [MI_OperationOptions_SetNumber function](..\mi\nf-mi-mi_operationoptions_setnumber.md) | Sets a custom number option value. |
| [MI_OperationOptions_SetPromptUserMode function](..\mi\nf-mi-mi_operationoptions_setpromptusermode.md) | Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function. |
| [MI_OperationOptions_SetPromptUserRegularMode function](..\mi\nf-mi-mi_operationoptions_setpromptuserregularmode.md) | Sets the value that tells the server how to respond to a provider's call to the MI_Context_PromptUser function. |
| [MI_OperationOptions_SetProviderArchitecture function](..\mi\nf-mi-mi_operationoptions_setproviderarchitecture.md) | Sets the provider architecture for an operation. |
| [MI_OperationOptions_SetResourceUri function](..\mi\nf-mi-mi_operationoptions_setresourceuri.md) | Sets the resource URI to use for an operation. |
| [MI_OperationOptions_SetResourceUriPrefix function](..\mi\nf-mi-mi_operationoptions_setresourceuriprefix.md) | Sets the resource URI prefix to use for an operation. |
| [MI_OperationOptions_SetString function](..\mi\nf-mi-mi_operationoptions_setstring.md) | Sets a custom string option. |
| [MI_OperationOptions_SetTimeout function](..\mi\nf-mi-mi_operationoptions_settimeout.md) | Sets the operation timeout for a specific operation. |
| [MI_OperationOptions_SetUseMachineID function](..\mi\nf-mi-mi_operationoptions_setusemachineid.md) | Enables or disables the sending of machine identification information in the operation request. |
| [MI_OperationOptions_SetWriteErrorMode function](..\mi\nf-mi-mi_operationoptions_setwriteerrormode.md) | Sets the error reporting mode. |
| [MI_Operation_Cancel function](..\mi\nf-mi-mi_operation_cancel.md) | Cancels a running operation. |
| [MI_Operation_Close function](..\mi\nf-mi-mi_operation_close.md) | Closes an operation handle. |
| [MI_Operation_GetClass function](..\mi\nf-mi-mi_operation_getclass.md) | Gets a synchronous result for a class operation. |
| [MI_Operation_GetIndication function](..\mi\nf-mi-mi_operation_getindication.md) | Get the synchronous results from a subscription. |
| [MI_Operation_GetInstance function](..\mi\nf-mi-mi_operation_getinstance.md) | Gets a synchronous result for an instance operation. |
| [MI_Operation_GetSession function](..\mi\nf-mi-mi_operation_getsession.md) | Gets the session associated with an operation. |
| [MI_ParameterSet_GetMethodReturnType function](..\mi\nf-mi-mi_parameterset_getmethodreturntype.md) | Gets the method return type and qualifier set for a specified parameter set. |
| [MI_ParameterSet_GetParameter function](..\mi\nf-mi-mi_parameterset_getparameter.md) | Gets a method's parameter information based on a parameter name. |
| [MI_ParameterSet_GetParameterAt function](..\mi\nf-mi-mi_parameterset_getparameterat.md) | Gets a method's parameter information at the specified index. |
| [MI_ParameterSet_GetParameterCount function](..\mi\nf-mi-mi_parameterset_getparametercount.md) | Gets the number of parameters in a method's parameter set. |
| [MI_PropertySet_AddElement function](..\mi\nf-mi-mi_propertyset_addelement.md) | Adds a name to the property list. |
| [MI_PropertySet_Clear function](..\mi\nf-mi-mi_propertyset_clear.md) | Removes all names from the property list. Afterwards, the count is zero. This allows property lists to be reused (without having to be destructed and reconstructed). |
| [MI_PropertySet_Clone function](..\mi\nf-mi-mi_propertyset_clone.md) | Creates a copy of the specified property set on the heap. |
| [MI_PropertySet_ContainsElement function](..\mi\nf-mi-mi_propertyset_containselement.md) | Determines whether the property list contains the specified property name. |
| [MI_PropertySet_Delete function](..\mi\nf-mi-mi_propertyset_delete.md) | Deletes the specified property list that was constructed on the heap. |
| [MI_PropertySet_Destruct function](..\mi\nf-mi-mi_propertyset_destruct.md) | Deletes the specified property list that was constructed on the stack. |
| [MI_PropertySet_GetElementAt function](..\mi\nf-mi-mi_propertyset_getelementat.md) | Gets the element of a property set at the specified index. |
| [MI_PropertySet_GetElementCount function](..\mi\nf-mi-mi_propertyset_getelementcount.md) | Gets the number of elements in the specified property set. |
| [MI_QualifierSet_GetQualifier function](..\mi\nf-mi-mi_qualifierset_getqualifier.md) | Gets the qualifier information based on the given qualifier name. |
| [MI_QualifierSet_GetQualifierAt function](..\mi\nf-mi-mi_qualifierset_getqualifierat.md) | Gets a qualifier at the specified index. |
| [MI_QualifierSet_GetQualifierCount function](..\mi\nf-mi-mi_qualifierset_getqualifiercount.md) | Gets the number of qualifiers in a qualifier set. |
| [MI_Serializer_Close function](..\mi\nf-mi-mi_serializer_close.md) | Closes a serializer object and frees any internal memory associated with it. |
| [MI_Serializer_SerializeClass function](..\mi\nf-mi-mi_serializer_serializeclass.md) | Serializes an MI_Class into a buffer in the format specified when the serializer was created. Options can be passed into the flags to control if the class and all its parent classes are serialized, or just the child-most class. |
| [MI_Serializer_SerializeInstance function](..\mi\nf-mi-mi_serializer_serializeinstance.md) | Serializes an MI_Instance into a buffer in the format specified when the serializer was created. Options can be passed into the flags to control if the class is also serialized into the buffer as well as the instance. |
| [MI_Server_GetSystemName function](..\mi\nf-mi-mi_server_getsystemname.md) | Gets the system name for the server. |
| [MI_Server_GetVersion function](..\mi\nf-mi-mi_server_getversion.md) | Gets the value of the MI_VERSION macro used when generating the provider. |
| [MI_Session_AssociatorInstances function](..\mi\nf-mi-mi_session_associatorinstances.md) | Finds instances that are associated with the specific key instance. |
| [MI_Session_Close function](..\mi\nf-mi-mi_session_close.md) | Closes a session and releases all associated memory. |
| [MI_Session_CreateInstance function](..\mi\nf-mi-mi_session_createinstance.md) | Creates an instance on the server that the session represents. |
| [MI_Session_DeleteInstance function](..\mi\nf-mi-mi_session_deleteinstance.md) | Deletes an instance on the server represented by the session. |
| [MI_Session_EnumerateClasses function](..\mi\nf-mi-mi_session_enumerateclasses.md) | Enumerates the classes of a specified session. |
| [MI_Session_EnumerateInstances function](..\mi\nf-mi-mi_session_enumerateinstances.md) | Enumerate all instances (on the server represented by the session) that are associated with a class. |
| [MI_Session_GetApplication function](..\mi\nf-mi-mi_session_getapplication.md) | Gets the application handle that was used to create the specified session. |
| [MI_Session_GetClass function](..\mi\nf-mi-mi_session_getclass.md) | Gets an MI_Class declaration based on a specific class name. |
| [MI_Session_GetInstance function](..\mi\nf-mi-mi_session_getinstance.md) | Gets the specified instance from the server represented by the session. |
| [MI_Session_Invoke function](..\mi\nf-mi-mi_session_invoke.md) | Invokes a method in the provider. |
| [MI_Session_ModifyInstance function](..\mi\nf-mi-mi_session_modifyinstance.md) | Updates an existing instance in the server represented by the session. |
| [MI_Session_QueryInstances function](..\mi\nf-mi-mi_session_queryinstances.md) | Queries for a set of instances based on a query expression. |
| [MI_Session_ReferenceInstances function](..\mi\nf-mi-mi_session_referenceinstances.md) | Finds the association object that references the specified key instance. |
| [MI_Session_Subscribe function](..\mi\nf-mi-mi_session_subscribe.md) | Subscribes to an indication on the server represented by the session. |
| [MI_Session_TestConnection function](..\mi\nf-mi-mi_session_testconnection.md) | Tests a connection by communicating with the server represented by the session to determine whether it is responding. |
| [MI_SubscriptionDeliveryOptions_AddDeliveryCredentials function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_adddeliverycredentials.md) | Sets a subscription option for delivery credentials to use when connecting back to the client to deliver a push indication result. |
| [MI_SubscriptionDeliveryOptions_Clone function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_clone.md) | Creates a copy of a MI_SubscriptionDeliveryOptions structure. |
| [MI_SubscriptionDeliveryOptions_Delete function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_delete.md) | Deletes the specified subscription delivery options structure. |
| [MI_SubscriptionDeliveryOptions_GetBookmark function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getbookmark.md) | Gets a previously set subscription bookmark. |
| [MI_SubscriptionDeliveryOptions_GetCredentialsAt function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getcredentialsat.md) | Gets a previously added credential based on a specified index. |
| [MI_SubscriptionDeliveryOptions_GetCredentialsCount function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getcredentialscount.md) | Gets the number of previously added credentials. |
| [MI_SubscriptionDeliveryOptions_GetCredentialsPasswordAt function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getcredentialspasswordat.md) | Gets a previously added credential password based on a specified index. |
| [MI_SubscriptionDeliveryOptions_GetDateTime function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getdatetime.md) | Gets a previously set datetime option. |
| [MI_SubscriptionDeliveryOptions_GetDeliveryDestination function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getdeliverydestination.md) | Gets the previously set subscription delivery destination. |
| [MI_SubscriptionDeliveryOptions_GetDeliveryPortNumber function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getdeliveryportnumber.md) | Gets the previously set delivery port number. |
| [MI_SubscriptionDeliveryOptions_GetDeliveryRetryAttempts function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryattempts.md) | Gets the number of delivery retry attempts. |
| [MI_SubscriptionDeliveryOptions_GetDeliveryRetryInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getdeliveryretryinterval.md) | Gets the delivery retry interval&#8212;the amount of time to wait before retrying the delivery. |
| [MI_SubscriptionDeliveryOptions_GetExpirationTime function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getexpirationtime.md) | Gets the delivery expiration value (which can be expressed as a timestamp or an interval). |
| [MI_SubscriptionDeliveryOptions_GetHeartbeatInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getheartbeatinterval.md) | Gets the delivery heartbeat interval. |
| [MI_SubscriptionDeliveryOptions_GetInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getinterval.md) | Gets the delivery interval for a specified option. |
| [MI_SubscriptionDeliveryOptions_GetMaximumLatency function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getmaximumlatency.md) | Gets the maximum amount of time that the server will hold a result before delivering it to the client. |
| [MI_SubscriptionDeliveryOptions_GetNumber function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getnumber.md) | Gets the value of the named numeric option. |
| [MI_SubscriptionDeliveryOptions_GetOption function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getoption.md) | Gets the value of the named option. |
| [MI_SubscriptionDeliveryOptions_GetOptionAt function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getoptionat.md) | Gets the option at the specified index. |
| [MI_SubscriptionDeliveryOptions_GetOptionCount function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getoptioncount.md) | Gets the number of previously set options. |
| [MI_SubscriptionDeliveryOptions_GetString function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_getstring.md) | Gets the value of the named string option. |
| [MI_SubscriptionDeliveryOptions_SetBookmark function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setbookmark.md) | Sets a bookmark for subscription indication delivery. |
| [MI_SubscriptionDeliveryOptions_SetDateTime function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setdatetime.md) | Sets the value of a named DateTime option. |
| [MI_SubscriptionDeliveryOptions_SetDeliveryDestination function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setdeliverydestination.md) | Sets the destination endpoint that an indication will be delivered to. |
| [MI_SubscriptionDeliveryOptions_SetDeliveryPortNumber function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setdeliveryportnumber.md) | Sets the subscription delivery port number. |
| [MI_SubscriptionDeliveryOptions_SetDeliveryRetryAttempts function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryattempts.md) | Sets the number of times a push delivery subscription will try to deliver a result. |
| [MI_SubscriptionDeliveryOptions_SetDeliveryRetryInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setdeliveryretryinterval.md) | Sets the delivery retry interval for subscriptions that are for push delivery. |
| [MI_SubscriptionDeliveryOptions_SetExpirationTime function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setexpirationtime.md) | Sets the subscription expiration time (when the subscription will shut down). |
| [MI_SubscriptionDeliveryOptions_SetHeartbeatInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setheartbeatinterval.md) | Sets the heartbeat interval. |
| [MI_SubscriptionDeliveryOptions_SetInterval function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setinterval.md) | Sets the value of a named interval option. |
| [MI_SubscriptionDeliveryOptions_SetMaximumLatency function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setmaximumlatency.md) | Sets the maximum amount of time that the server will hold a result before delivering it to the client. |
| [MI_SubscriptionDeliveryOptions_SetNumber function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setnumber.md) | Sets the value of a named numeric option that is not covered by a dedicated function. |
| [MI_SubscriptionDeliveryOptions_SetString function](..\mi\nf-mi-mi_subscriptiondeliveryoptions_setstring.md) | Sets the value of a named string option that is not covered by a dedicated function. |
| [MI_Utilities_CimErrorFromErrorCode function](..\mi\nf-mi-mi_utilities_cimerrorfromerrorcode.md) | Maps an operating-system specific error code to a CIM error instance. |
| [MI_Utilities_MapErrorToMiErrorCategory function](..\mi\nf-mi-mi_utilities_maperrortomierrorcategory.md) | Maps an operating system specific error code to an error category. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [MI_Deserializer_ClassObjectNeeded callback function](..\mi\nc-mi-mi_deserializer_classobjectneeded.md) | Used to provide requested class object during deserialization. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_MI_Application structure](..\mi\ns-mi-_mi_application.md) | Represents the initialized infrastructure. |
| [_MI_ApplicationFT structure](..\mi\ns-mi-_mi_applicationft.md) | A support structure used in the MI_Application structure. Use the functions with the name prefix &#0034;MI_Application_&#0034; to manipulate these structures. |
| [_MI_Array structure](..\mi\ns-mi-_mi_array.md) | Generalized type that represents an array. It can be generalized because all arrays are the same size, except the data element type will be specialized. |
| [_MI_ArrayField structure](..\mi\ns-mi-_mi_arrayfield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_BooleanA structure](..\mi\ns-mi-_mi_booleana.md) | Represents an array of MI_Boolean types. |
| [_MI_BooleanAField structure](..\mi\ns-mi-_mi_booleanafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_BooleanField structure](..\mi\ns-mi-_mi_booleanfield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Char16A structure](..\mi\ns-mi-_mi_char16a.md) | Represents an array of MI_Char16 types. |
| [_MI_Char16AField structure](..\mi\ns-mi-_mi_char16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Char16Field structure](..\mi\ns-mi-_mi_char16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Class structure](..\mi\ns-mi-_mi_class.md) | Represents the schema of an instance. |
| [_MI_ClassDecl structure](..\mi\ns-mi-_mi_classdecl.md) | This structure outlines the class declaration. It contains class name and hierarchy, properties, qualifiers, and methods. |
| [_MI_ClassFT structure](..\mi\ns-mi-_mi_classft.md) | A support structure used in the MI_Class structure. Use the functions with the name prefix &#0034;MI_Class_&#0034; to manipulate these structures. |
| [_MI_ClientFT_V1 structure](..\mi\ns-mi-_mi_clientft_v1.md) | Client function tables. |
| [_MI_ConstBooleanA structure](..\mi\ns-mi-_mi_constbooleana.md) | Represents an array of MI_ConstBoolean types. |
| [_MI_ConstBooleanAField structure](..\mi\ns-mi-_mi_constbooleanafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstBooleanField structure](..\mi\ns-mi-_mi_constbooleanfield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstChar16A structure](..\mi\ns-mi-_mi_constchar16a.md) | Represents an array of MI_Char16 types. |
| [_MI_ConstChar16AField structure](..\mi\ns-mi-_mi_constchar16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstChar16Field structure](..\mi\ns-mi-_mi_constchar16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstDatetimeA structure](..\mi\ns-mi-_mi_constdatetimea.md) | Represents an array of MI_Datatime types. |
| [_MI_ConstDatetimeAField structure](..\mi\ns-mi-_mi_constdatetimeafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstDatetimeField structure](..\mi\ns-mi-_mi_constdatetimefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstInstanceA structure](..\mi\ns-mi-_mi_constinstancea.md) | Represents an array of MI_Instance types. |
| [_MI_ConstInstanceAField structure](..\mi\ns-mi-_mi_constinstanceafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstInstanceField structure](..\mi\ns-mi-_mi_constinstancefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReal32A structure](..\mi\ns-mi-_mi_constreal32a.md) | Represents an array of MI_Real32 types. |
| [_MI_ConstReal32AField structure](..\mi\ns-mi-_mi_constreal32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReal32Field structure](..\mi\ns-mi-_mi_constreal32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReal64A structure](..\mi\ns-mi-_mi_constreal64a.md) | Represents an array of MI_Real64 types. |
| [_MI_ConstReal64AField structure](..\mi\ns-mi-_mi_constreal64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReal64Field structure](..\mi\ns-mi-_mi_constreal64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReferenceA structure](..\mi\ns-mi-_mi_constreferencea.md) | Represents an array of MI_Instance types. |
| [_MI_ConstReferenceAField structure](..\mi\ns-mi-_mi_constreferenceafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstReferenceField structure](..\mi\ns-mi-_mi_constreferencefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint16A structure](..\mi\ns-mi-_mi_constsint16a.md) | Represents an array of MI_Sint16 types. |
| [_MI_ConstSint16AField structure](..\mi\ns-mi-_mi_constsint16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint16Field structure](..\mi\ns-mi-_mi_constsint16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint32A structure](..\mi\ns-mi-_mi_constsint32a.md) | Represents an array of MI_Sint32 types. |
| [_MI_ConstSint32AField structure](..\mi\ns-mi-_mi_constsint32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint32Field structure](..\mi\ns-mi-_mi_constsint32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint64A structure](..\mi\ns-mi-_mi_constsint64a.md) | Represents an array of MI_Sint64 types. |
| [_MI_ConstSint64AField structure](..\mi\ns-mi-_mi_constsint64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint64Field structure](..\mi\ns-mi-_mi_constsint64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint8A structure](..\mi\ns-mi-_mi_constsint8a.md) | Represents an array of MI_Sint8 types. |
| [_MI_ConstSint8AField structure](..\mi\ns-mi-_mi_constsint8afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstSint8Field structure](..\mi\ns-mi-_mi_constsint8field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstStringA structure](..\mi\ns-mi-_mi_conststringa.md) | Represents an array of MI_Char types. |
| [_MI_ConstStringAField structure](..\mi\ns-mi-_mi_conststringafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstStringField structure](..\mi\ns-mi-_mi_conststringfield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint16A structure](..\mi\ns-mi-_mi_constuint16a.md) | Represents an array of MI_Uint16A types. |
| [_MI_ConstUint16AField structure](..\mi\ns-mi-_mi_constuint16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint16Field structure](..\mi\ns-mi-_mi_constuint16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint32A structure](..\mi\ns-mi-_mi_constuint32a.md) | Represents an array of MI_Uint32 types. |
| [_MI_ConstUint32AField structure](..\mi\ns-mi-_mi_constuint32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint32Field structure](..\mi\ns-mi-_mi_constuint32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint64A structure](..\mi\ns-mi-_mi_constuint64a.md) | Represents an array of MI_Uint64 types. |
| [_MI_ConstUint64AField structure](..\mi\ns-mi-_mi_constuint64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint64Field structure](..\mi\ns-mi-_mi_constuint64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint8A structure](..\mi\ns-mi-_mi_constuint8a.md) | Represents an array of MI_Uint8 types. |
| [_MI_ConstUint8AField structure](..\mi\ns-mi-_mi_constuint8afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ConstUint8Field structure](..\mi\ns-mi-_mi_constuint8field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Context structure](..\mi\ns-mi-_mi_context.md) | Holds context for the operation that the provider needs to carry out. |
| [_MI_ContextFT structure](..\mi\ns-mi-_mi_contextft.md) | A support structure used in the MI_Context structure. Use the functions with the name prefix &#0034;MI_Context_&#0034; to manipulate these structures. |
| [_MI_Datetime structure](..\mi\ns-mi-_mi_datetime.md) | Represents a union of MI_Timestamp and MI_Interval. |
| [_MI_DatetimeA structure](..\mi\ns-mi-_mi_datetimea.md) | Represents an array of MI_Datetime types. |
| [_MI_DatetimeAField structure](..\mi\ns-mi-_mi_datetimeafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_DatetimeField structure](..\mi\ns-mi-_mi_datetimefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Deserializer structure](..\mi\ns-mi-_mi_deserializer.md) | Deserialization object as created from MI_Application_NewDeserializer. The object itself should not be manually used or changed as it is used internally. |
| [_MI_DeserializerFT structure](..\mi\ns-mi-_mi_deserializerft.md) | A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Deserializer_&#0034; to manipulate these structures. |
| [_MI_DestinationOptions structure](..\mi\ns-mi-_mi_destinationoptions.md) | Represents a set of destination options. Destination options are a set of configurations that define the way an operation communicates with the server. |
| [_MI_DestinationOptionsFT structure](..\mi\ns-mi-_mi_destinationoptionsft.md) | A support structure used in the MI_DestinationOptions structure. Use the functions with the name prefix &#0034;MI_DestinationOptions_&#0034; to manipulate these structures. |
| [_MI_FeatureDecl structure](..\mi\ns-mi-_mi_featuredecl.md) | Contains properties that are common to the MI_PropertyDeclMI_ParameterDecl and MI_MethodDecl structures. |
| [_MI_Filter structure](..\mi\ns-mi-_mi_filter.md) | Contains a reference to the function table MI_FilterFT. |
| [_MI_FilterFT structure](..\mi\ns-mi-_mi_filterft.md) | A support structure used in the MI_Filter structure. Use the functions with the name prefix &#0034;MI_Filter_&#0034; to manipulate these structures. |
| [_MI_HostedProvider structure](..\mi\ns-mi-_mi_hostedprovider.md) | Represents the hosting of a provider in a client application. |
| [_MI_HostedProviderFT structure](..\mi\ns-mi-_mi_hostedproviderft.md) | A support structure used in the MI_HostedProvider structure. Use the functions with the name prefix &#0034;MI_HostedProvider_&#0034; to manipulate these structures. |
| [_MI_Instance structure](..\mi\ns-mi-_mi_instance.md) | This structure represents a CIM instance. This object should not be accessed directly. Instead, the MI_Instance_* functions should be used. |
| [_MI_InstanceA structure](..\mi\ns-mi-_mi_instancea.md) | Represents an array of MI_Instance structures. |
| [_MI_InstanceAField structure](..\mi\ns-mi-_mi_instanceafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_InstanceExFT structure](..\mi\ns-mi-_mi_instanceexft.md) | Extends the MI_InstanceFT structure. |
| [_MI_InstanceFT structure](..\mi\ns-mi-_mi_instanceft.md) | A support structure used in the MI_Instance structure. Use the functions with the name prefix MI_Instance_ to manipulate these structures. |
| [_MI_InstanceField structure](..\mi\ns-mi-_mi_instancefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Interval structure](..\mi\ns-mi-_mi_interval.md) | MI_Interval represents an interval of time. |
| [_MI_MethodDecl structure](..\mi\ns-mi-_mi_methoddecl.md) | Represents a CIM method. |
| [_MI_Module structure](..\mi\ns-mi-_mi_module.md) | Generated by the provider, this object contains all the data needed by the provider manager to manage the providers within this module. |
| [_MI_ObjectDecl structure](..\mi\ns-mi-_mi_objectdecl.md) | Contains properties common to the MI_ClassDecl and MI_PropertyDecl structures. |
| [_MI_Operation structure](..\mi\ns-mi-_mi_operation.md) | Represents a single operations execution. This object holds the internal function tables for carrying out actions on the operation. |
| [_MI_OperationCallbacks structure](..\mi\ns-mi-_mi_operationcallbacks.md) | Structure that holds all callback function pointers for carrying out operations. |
| [_MI_OperationFT structure](..\mi\ns-mi-_mi_operationft.md) | A support structure used in the MI_Operation structure. Use the functions with the name prefix &#0034;MI_Operation_&#0034; to manipulate these structures. |
| [_MI_OperationOptions structure](..\mi\ns-mi-_mi_operationoptions.md) | Represents a set of operation options. |
| [_MI_OperationOptionsFT structure](..\mi\ns-mi-_mi_operationoptionsft.md) | A support structure used in the MI_OperationOptions structure. Use the functions with the name prefix &#0034;MI_OperationOptions_&#0034; to manipulate these structures. |
| [_MI_ParameterDecl structure](..\mi\ns-mi-_mi_parameterdecl.md) | Represents CIM method parameters. |
| [_MI_ParameterSet structure](..\mi\ns-mi-_mi_parameterset.md) | Holds the method parameters of a class definition. |
| [_MI_ParameterSetFT structure](..\mi\ns-mi-_mi_parametersetft.md) | A support structure used in the MI_ParameterSet structure. Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures. |
| [_MI_PropertyDecl structure](..\mi\ns-mi-_mi_propertydecl.md) | Represents a class property (element) in a class's declaration. |
| [_MI_PropertySet structure](..\mi\ns-mi-_mi_propertyset.md) | Implements a set of property names. |
| [_MI_PropertySetFT structure](..\mi\ns-mi-_mi_propertysetft.md) | A support structure used in the MI_PropertySet structure. Use the functions with the name prefix &#0034;MI_PropertySet_&#0034; to manipulate these structures. |
| [_MI_ProviderFT structure](..\mi\ns-mi-_mi_providerft.md) | A support structure used in the MI_ClassDecl and MI_Module structures. |
| [_MI_Qualifier structure](..\mi\ns-mi-_mi_qualifier.md) | Represents a CIM qualifier. |
| [_MI_QualifierDecl structure](..\mi\ns-mi-_mi_qualifierdecl.md) | Represents a CIM qualifier declaration. |
| [_MI_QualifierSet structure](..\mi\ns-mi-_mi_qualifierset.md) | Allows the developer to view the qualifiers of a class definition. |
| [_MI_QualifierSetFT structure](..\mi\ns-mi-_mi_qualifiersetft.md) | A support structure used in the MI_QualifierSet structure. Use the functions with the name prefix &#0034;MI_QualifierSet_&#0034; to manipulate these structures. |
| [_MI_Real32A structure](..\mi\ns-mi-_mi_real32a.md) | Represents an array of MI_Real32 types. |
| [_MI_Real32AField structure](..\mi\ns-mi-_mi_real32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Real32Field structure](..\mi\ns-mi-_mi_real32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Real64A structure](..\mi\ns-mi-_mi_real64a.md) | Represents an array of MI_Real64 types. |
| [_MI_Real64AField structure](..\mi\ns-mi-_mi_real64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Real64Field structure](..\mi\ns-mi-_mi_real64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ReferenceA structure](..\mi\ns-mi-_mi_referencea.md) | Represents an array of pointers to MI_Instance types. |
| [_MI_ReferenceAField structure](..\mi\ns-mi-_mi_referenceafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_ReferenceField structure](..\mi\ns-mi-_mi_referencefield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_SchemaDecl structure](..\mi\ns-mi-_mi_schemadecl.md) | Represents the schema objects in a CIM schema, which include CIM classes and CIM qualifier declarations. |
| [_MI_Serializer structure](..\mi\ns-mi-_mi_serializer.md) | An object tied to a specific serialization technique. |
| [_MI_SerializerFT structure](..\mi\ns-mi-_mi_serializerft.md) | A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Serializer_&#0034; to manipulate these structures. |
| [_MI_Server structure](..\mi\ns-mi-_mi_server.md) | This structure defines default function tables for all types |
| [_MI_ServerFT structure](..\mi\ns-mi-_mi_serverft.md) | A support structure used in the MI_Server structure. Use the functions with the name prefix &#0034;MI_Server_&#0034; to manipulate these structures. |
| [_MI_Session structure](..\mi\ns-mi-_mi_session.md) | An object that is associated with a destination and has a set of credentials and options associated with it. . |
| [_MI_SessionCallbacks structure](..\mi\ns-mi-_mi_sessioncallbacks.md) | A container for callback function pointers that handle logging and error messages. |
| [_MI_SessionFT structure](..\mi\ns-mi-_mi_sessionft.md) | Function table for all actions on a session object. |
| [_MI_Sint16A structure](..\mi\ns-mi-_mi_sint16a.md) | Represents an array of MI_Sint16 types. |
| [_MI_Sint16AField structure](..\mi\ns-mi-_mi_sint16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint16Field structure](..\mi\ns-mi-_mi_sint16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint32A structure](..\mi\ns-mi-_mi_sint32a.md) | Represents an array of MI_Sint32 types. |
| [_MI_Sint32AField structure](..\mi\ns-mi-_mi_sint32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint32Field structure](..\mi\ns-mi-_mi_sint32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint64A structure](..\mi\ns-mi-_mi_sint64a.md) | Represents an array of MI_Sint64 types. |
| [_MI_Sint64AField structure](..\mi\ns-mi-_mi_sint64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint64Field structure](..\mi\ns-mi-_mi_sint64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint8A structure](..\mi\ns-mi-_mi_sint8a.md) | Represents an array of MI_Sint8 types. |
| [_MI_Sint8AField structure](..\mi\ns-mi-_mi_sint8afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Sint8Field structure](..\mi\ns-mi-_mi_sint8field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_StringA structure](..\mi\ns-mi-_mi_stringa.md) | Represents an array of pointers to null-terminated MI_Char* strings. |
| [_MI_StringAField structure](..\mi\ns-mi-_mi_stringafield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_StringField structure](..\mi\ns-mi-_mi_stringfield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_SubscriptionDeliveryOptions structure](..\mi\ns-mi-_mi_subscriptiondeliveryoptions.md) | The subscription options object stores configuration options used for passing into subscription operations. |
| [_MI_SubscriptionDeliveryOptionsFT structure](..\mi\ns-mi-_mi_subscriptiondeliveryoptionsft.md) | A support structure used in the MI_SubscriptionDeliveryOptions structure. Use the functions with the name prefix &#0034;MI_SubscriptionDeliveryOptions_&#0034; to manipulate these structures. |
| [_MI_Timestamp structure](..\mi\ns-mi-_mi_timestamp.md) | MI_Timestamp specifies a timestamp or a specific point in time. |
| [_MI_Uint16A structure](..\mi\ns-mi-_mi_uint16a.md) | Represents an array of MI_Uint16 types. |
| [_MI_Uint16AField structure](..\mi\ns-mi-_mi_uint16afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint16Field structure](..\mi\ns-mi-_mi_uint16field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint32A structure](..\mi\ns-mi-_mi_uint32a.md) | Represents an array of MI_Uint32 types. |
| [_MI_Uint32AField structure](..\mi\ns-mi-_mi_uint32afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint32Field structure](..\mi\ns-mi-_mi_uint32field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint64A structure](..\mi\ns-mi-_mi_uint64a.md) | Represents an array of MI_Uint64 types. |
| [_MI_Uint64AField structure](..\mi\ns-mi-_mi_uint64afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint64Field structure](..\mi\ns-mi-_mi_uint64field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint8A structure](..\mi\ns-mi-_mi_uint8a.md) | Represents an array of MI_Uint8 types. |
| [_MI_Uint8AField structure](..\mi\ns-mi-_mi_uint8afield.md) | Represents a property inside an MI_Instance structure. |
| [_MI_Uint8Field structure](..\mi\ns-mi-_mi_uint8field.md) | Represents a property inside an MI_Instance structure. |
| [_MI_UserCredentials structure](..\mi\ns-mi-_mi_usercredentials.md) | A user's credentials. It includes an authentication type and either a username and password or a certificate thumbprint. |
| [_MI_UsernamePasswordCreds structure](..\mi\ns-mi-_mi_usernamepasswordcreds.md) | A username/password combination used for subscription operations. |
| [_MI_UtilitiesFT structure](..\mi\ns-mi-_mi_utilitiesft.md) | A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &#0034;MI_Utilities_&#0034; to manipulate these structures. |
| [_MI_Value structure](..\mi\ns-mi-_mi_value.md) | A union of all CIM data types. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_MI_CallbackMode enumeration](..\mi\ne-mi-_mi_callbackmode.md) | Defines the callback mode for the CIM extensions for WriteError and PromptUser functions. |
| [_MI_CancellationReason enumeration](..\mi\ne-mi-_mi_cancellationreason.md) | Value to pass to an operation cancel request to notify the system of the reason the operation is being canceled. If the service is being shutdown, it may pass one of these values to the provider as well. |
| [_MI_DestinationOptions_ImpersonationType enumeration](..\mi\ne-mi-_mi_destinationoptions_impersonationtype.md) | Used by the DCOM protocol handler to specify how impersonation is done on the server. |
| [_MI_ErrorCategory enumeration](..\mi\ne-mi-_mi_errorcategory.md) | This enumeration defines error categories for the CIM extensions. |
| [_MI_LocaleType enumeration](..\mi\ne-mi-_mi_localetype.md) | Type of locale is needed when setting and getting locales. |
| [_MI_OperationCallback_ResponseType enumeration](..\mi\ne-mi-_mi_operationcallback_responsetype.md) | If the MI_CallbackMode is MI_CALLBACKMODE_INQUIRE, one of these values can be used in the callback. |
| [_MI_PromptType enumeration](..\mi\ne-mi-_mi_prompttype.md) | Defines prompt types for the CIM extensions. |
| [_MI_ProviderArchitecture enumeration](..\mi\ne-mi-_mi_providerarchitecture.md) | This enumeration defines the WMI provider architecture used on the server. |
| [_MI_Result enumeration](..\mi\ne-mi-_mi_result.md) | Defines function return codes. |
| [_MI_SubscriptionDeliveryType enumeration](..\mi\ne-mi-_mi_subscriptiondeliverytype.md) | Differentiates between a push or pull subscription delivery type. This is not supported when using the DCOM protocol. |
| [_MI_Type enumeration](..\mi\ne-mi-_mi_type.md) | These values specify the data type of qualifiers, properties, references, parameters, and method return values for the CIM data types. |
